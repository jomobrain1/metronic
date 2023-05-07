<template>
  <div class="card p-5 my-5">
    <h5>Files</h5>
    <!-- Files -->
    <FileCard filename="File name" file_property="property name"></FileCard>
    <FileCard filename="Another Name" file_property="property name"></FileCard>
    <FileCard filename="This Name" file_property="properties"></FileCard>
    <FileCard filename="File name" file_property="file size"></FileCard>
  </div>
</template>

<script setup lang="ts">
import FileCard from "./FileCard.vue";
</script>
