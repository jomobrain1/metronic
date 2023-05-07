<template>
  <div class="row">
    <section class="card py-5 px-2 col-lg-4 mb-5 col-md-4">
      <!-- Left Pane -->
      <LeftPane></LeftPane>
    </section>
    <section class="col-lg-8 col-md-8">
      <RightPane></RightPane>
    </section>
  </div>
</template>

<script lang="ts" setup>
import LeftPane from "./streams/LeftPane.vue";
import RightPane from "./streams/RightPane.vue";
</script>
