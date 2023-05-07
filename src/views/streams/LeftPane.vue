<template>
  <CalendarApp1Vue></CalendarApp1Vue>
  <EventOne></EventOne>
  <EventTwo></EventTwo>
</template>
<script lang="ts" setup>
import CalendarApp1Vue from "@/components/calendar/CalendarApp1.vue";
import EventOne from "./leftpanes/EventOne.vue";
import EventTwo from "./leftpanes/EventTwo.vue";
</script>

<style>
.fc-toolbar-title {
  font-size: 15px !important;
}

.fc .fc-toolbar {
  display: flex;
  align-items: center;
  flex-direction: column;
  justify-content: space-evenly;
}
.fc-toolbar-chunk:first-child {
  width: 100%;
  display: flex;

  justify-content: space-between;
}
.fc-toolbar-chunk:nth-child(2) {
  margin: 5px 3px 5px;
}
</style>
