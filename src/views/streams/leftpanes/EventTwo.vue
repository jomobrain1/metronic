<template>
  <h5 class="text-center my-2 head">Fri, April 2023</h5>

  <Event
    icon="faceid"
    title="this meeting"
    time="7:30pm"
    comment="Not in vlog"
  ></Event>
  <Event
    icon="electricity"
    title="great meeting"
    time="8:30pm"
    comment="Not in vlog"
  ></Event>
  <Event
    icon="artificial-intelligence"
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
