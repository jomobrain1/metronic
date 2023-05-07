<template>
  <div class="row my-3">
    <div class="col-md-2 rounded p-2 bg-secondary">
      <img class="w-100 rounded" src="https://picsum.photos/200" alt="" />
    </div>
    <div class="col-md-10">
      <div class="row">
        <div class="col-md-8">
          <h6>
            <span class="me-2">{{ title }}</span>
            <small class="at"><b>{{ at }}</b></small>
          </h6>
        </div>
        <section class="col-md-4">
          <p class="fw-bold">Reply</p>
        </section>
      </div>
      <p>{{ paragraph }}</p>
    </div>
  </div>
</template>

<script lang="ts">
export default {
props:["title","at","paragraph"]
};
</script>

<style lang="scss" scoped>
.at{
  color: rgba(0,0,0,.4);
}
</style>
