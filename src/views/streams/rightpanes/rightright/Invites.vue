<template>
  <section class="card p-5">
    <div class="d-flex p-4 align-items-center justify-content-between">
      <h5>Invites <small>(5)</small></h5>
      <button class="btn btn-sm">Invite</button>
    </div>
    <!-- Invites -->
    <FileCard filename="Invite One" file_property="jomo brain"></FileCard>
    <FileCard filename="Invite One" file_property="jomo brain"></FileCard>
    <FileCard filename="Invite One" file_property="jomo brain"></FileCard>
    <FileCard filename="Invite One" file_property="jomo brain"></FileCard>
  </section>
</template>

<script setup lang="ts">
import FileCard from "./FileCard.vue";
</script>
