<template>
  <div class="d-flex px-2 text-start justify-content-start align-items-center">
    <section class="bg-secondary p-2 me-5 rounded">
      <img width="30" src="https://picsum.photos/200" alt="" />
    </section>
    <div class="py-2">
      <b>{{ filename }}</b>
      <p>{{ file_property }}</p>
    </div>
  </div>
</template>

<script>
export default {
    props:["filename","file_property"]
};
</script>

<style lang="scss" scoped></style>
