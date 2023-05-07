<template>
  <section class="card">
    <StreamCard>
      <template v-slot:header>
        <div class="d-flex justify-content-between align-items-center px-3">
          <h3>Streams</h3>

          <h6 class="btn btn-sm fw-bold btn-primary" role="button">
            + New Stream
          </h6>
        </div>
      </template>
    </StreamCard>
  </section>
</template>

<script lang="ts" setup>
import StreamCard from "./StreamCard.vue";
</script>
