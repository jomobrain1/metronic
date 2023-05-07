<template>
  <div class="px-3">
    <section class="row">
      <div class="col-8">
        <div class="d-flex">
          <div class="">
            <section class="bg-secondary p-2 mx-3 rounded">
              <KTIcon
                :icon-name="icon"
                icon-class="fs-2"
                class="text-primary"
              />
            </section>
          </div>
          <div class="mx-3">
            <b>{{ title }}</b>
            <p>{{ time }}</p>
          </div>
        </div>
      </div>
      <div class="col-4 d-flex align-items-center">
        <small>{{ comment }}</small>
      </div>
    </section>
  </div>
</template>

<script lang="ts">
export default {
  props: ["title", "time", "comment", "icon"],
};
</script>
