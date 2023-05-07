<template>
  <div
    class="modal fade show"
    id="kt_modal_add_event1"
    aria-modal="true"
    role="dialog"
    ref="newTargetModalRef"
  >
    <div class="modal-dialog modal-dialog-centered modal-size">
      <div class="modal-content">
        <div class="modal-header">
          <h2 class="fw-bold">Create a New Event</h2>
          <div
            class="btn btn-icon btn-sm btn-active-icon-primary"
            id="kt_modal_add_event_close"
            data-bs-dismiss="modal"
          >
            <KTIcon icon-name="cross" icon-class="fs-1" />
          </div>
        </div>

        <section class="row">
          <div class="col-md-4">
            <LeftPane></LeftPane>
          </div>

          <div class="col-md-8">
            <RightPane></RightPane>
          </div>
        </section>
      </div>
    </div>
  </div>
</template>

<script lang="ts">
import { getAssetPath } from "@/core/helpers/assets";
import { defineComponent, ref } from "vue";
import { hideModal } from "@/core/helpers/dom";
import Swal from "sweetalert2/dist/sweetalert2.js";
import LeftPane from "./newevent/LeftPane.vue";
import RightPane from "./newevent/RightPane.vue";
interface NewAddressData {
  eventName: string;
  eventDescription: string;
  eventLocation: string;
  allDay: boolean;
  eventStartDate: string;
  eventEndDate: string;
}

export default defineComponent({
  name: "new-event-modal",
  components: {
    LeftPane,
    RightPane,
  },
  setup() {
    const formRef = ref<null | HTMLFormElement>(null);
    const newTargetModalRef = ref<null | HTMLElement>(null);
    const loading = ref<boolean>(false);

    const targetData = ref<NewAddressData>({
      eventName: "",
      eventDescription: "",
      eventLocation: "",
      allDay: true,
      eventStartDate: "",
      eventEndDate: "",
    });

    const rules = ref({
      eventName: [
        {
          required: true,
          message: "Please input event name",
          trigger: "blur",
        },
      ],
    });

    const submit = () => {
      if (!formRef.value) {
        return;
      }

      formRef.value.validate((valid: boolean) => {
        if (valid) {
          loading.value = true;

          setTimeout(() => {
            loading.value = false;

            Swal.fire({
              text: "Form has been successfully submitted!",
              icon: "success",
              buttonsStyling: false,
              confirmButtonText: "Ok, got it!",
              heightAuto: false,
              customClass: {
                confirmButton: "btn btn-primary",
              },
            }).then(() => {
              hideModal(newTargetModalRef.value);
            });
          }, 2000);
        } else {
          Swal.fire({
            text: "Sorry, looks like there are some errors detected, please try again.",
            icon: "error",
            buttonsStyling: false,
            confirmButtonText: "Ok, got it!",
            heightAuto: false,
            customClass: {
              confirmButton: "btn btn-primary",
            },
          });
          return false;
        }
      });
    };

    return {
      formRef,
      newTargetModalRef,
      loading,
      targetData,
      rules,
      submit,
      getAssetPath,
    };
  },
});
</script>

<style lang="scss">
.el-select {
  width: 100%;
}

.el-date-editor.el-input,
.el-date-editor.el-input__inner {
  width: 100%;
}
.modal-size {
  min-width: 80vw;
}
</style>
