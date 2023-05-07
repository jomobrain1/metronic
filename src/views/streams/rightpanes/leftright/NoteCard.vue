<template>
  <div class="col-md-12">
    <div class="shadow p-3 mb-5 bg-body-tertiary rounded">
      <section class="d-flex justify-content-between">
        <h5 class="">This is Heading</h5>
        <p class="">
          <KTIcon icon-name="pencil" icon-class="fs-2" class="text-dark" />
        </p>
      </section>
      <slot> </slot>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style scoped></style>
