<template>
  <div class="my-3 row p-5">
    <NoteCard>
      Lorem ipsum dolor sit amet consectetur adipisicing elit. Pariatur ipsam
      dolore eos dolorum veniam mollitia rem id quae harum eligendi. Possimus
      nulla similique repudiandae provident, laboriosam molestias odit est
      nesciunt?
    </NoteCard>
    <NoteCard>
      has survived not only five centuries, but also the leap into electronic
      typesetting, remaining essentially unchanged. It was popularised in the
      1960s with the release of Letraset sheets containing Lorem Ipsum passages,
      and more recently with desktop publishing software like Aldus PageMaker
      including versions of Lorem Ipsum.?
    </NoteCard>

    <Editor></Editor>
  </div>
</template>

<script setup lang="ts">
import NoteCard from "./NoteCard.vue";
import Editor from "./Editor.vue";
</script>
