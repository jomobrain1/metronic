<template>
  <div class="px-3">
    <Notes></Notes>
    <ChatFeed></ChatFeed>
    <CommentSection></CommentSection>
    <Videos></Videos>
    <VideosComment></VideosComment>
  </div>
</template>

<script lang="ts" setup>
import ChatFeed from "./leftright/ChatFeed.vue";
import Videos from "./leftright/Videos.vue";
import VideosComment from "./leftright/VideosComment.vue";

import CommentSection from "./leftright/CommentSection.vue";
import Notes from "./leftright/Notes.vue";
</script>
