<template>
    <div class="">
      <div class="py-3 px-5">
        <section id="stream-card-header">
          <slot name="header"></slot>
        </section>
        <section id="stream-card-content">
          <slot></slot>
        </section>
        <section id="stream-card-footer">
          <slot name="footer"> </slot>
        </section>
      </div>
    </div>
    </template>
    
    <script lang="ts" setup></script>
    