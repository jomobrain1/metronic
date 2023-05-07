<template>
  <div class="my-3 row p-5">
    <Editor></Editor>
    <NoteCard>
      <Note1></Note1>
    </NoteCard>
    <NoteCard>
      has survived not only five centuries, but also the leap into electronic
      typesetting, remaining essentially unchanged. It was popularised in the
      1960s with the release of Letraset sheets containing Lorem Ipsum passages,
      and more recently with desktop publishing software like Aldus PageMaker
      including versions of Lorem Ipsum.?
    </NoteCard>
  </div>
</template>

<script setup lang="ts">
import NoteCard from "./NoteCard.vue";
import Note1 from "./Note1.vue";
import Editor from "./Editor.vue";
</script>
