<template>
  <div class="shadow p-3 mb-5 bg-body-tertiary rounded">
    <div>
      <TopBox></TopBox>
      <Liner></Liner>
      <div class="row my-3">
        <div class="col-md-4">
          <img
            class="w-100"
            width=""
            height="100"
            src="https://picsum.photos/200/300?grayscale"
            alt=""
            srcset=""
          />
          <div class="py-3 d-flex justify-content-evenly">
            <span>12:00</span> <b>Marketing</b>
          </div>
        </div>
        <div class="col-md-4">
          <img
            class="w-100 rounded"
            width=""
            height="100"
            src="https://picsum.photos/200/300?grayscale"
            alt=""
            srcset=""
          />
          <div class="py-3 d-flex justify-content-evenly">
            <span>12:00</span> <b>Technology</b>
          </div>
        </div>
        <div class="col-md-4">
          <img
            class="w-100 rounded"
            width=""
            height="100"
            src="https://picsum.photos/200/300?grayscale"
            alt=""
            srcset=""
          />
          <div class="py-3 d-flex justify-content-evenly">
            <span>12:00</span> <b>Business</b>
          </div>
        </div>
      </div>

      <CommentsCounts></CommentsCounts>
    </div>
  </div>
</template>

<script lang="ts" setup>
import TopBox from "./TopBox.vue";
import Liner from "./Liner.vue";
import CommentsCounts from "./CommentsCounts.vue";
</script>
