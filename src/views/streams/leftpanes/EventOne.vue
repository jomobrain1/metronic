<template>
  <h5 class="text-center my-2 head">Wed, April 2023</h5>
  <Event
    icon="plus"
    title="some meeting"
    time="6:30pm"
    comment="Not in vlog"
  ></Event>
  <Event
    icon="design-2"
    title="another meeting"
    time="7:30pm"
    comment="Not in vlog"
  ></Event>
  <Event
    icon="design-mask"
    title="awesome meeting"
    time="8:30pm"
    comment="Not in vlog"
  ></Event>
  <Event
    icon="fasten"
    title="good meeting"
    time="9:30pm"
    comment="Not in vlog"
  ></Event>
</template>
<script lang="ts" setup>
import Event from "./Event.vue";
</script>
<style>
.head {
  color: #a0a0a0;
}
</style>
