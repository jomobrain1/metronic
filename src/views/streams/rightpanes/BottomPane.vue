<template>
  <section class="row mx-auto ">
    <div class="col-md-8 shadow p-3 my-5 bg-body-tertiary rounded">
      <LeftRightPane></LeftRightPane>
    </div>
    <div class="col-md-4">
      <RightRightPane></RightRightPane>
    </div>
  </section>
</template>

<script lang="ts" setup>
import LeftRightPane from "./LeftRightPane.vue";
import RightRightPane from "./RightRightPane.vue";
</script>
