<template>
  <div class="col-md-12">
    <div class="shadow p-5 mb-5 bg-body-tertiary rounded">
      <section class="d-flex justify-content-between">
        <h3>This is Note Heading</h3>
        <KTIcon icon-name="pencil" icon-class="fs-2" class="text-dark" />
      </section>
      <div class="liner mb-5"></div>

      <section class="px-5">
        <slot> </slot>
      </section>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style>
.liner {
  width: 100%;
  height: 2px;
  margin-bottom: 30px;

  /* background: #a0a0a0; */
}
</style>
