<template>
  <div class="shadow p-5 mb-5 bg-body-tertiary rounded">
    <div>
      <TopBox></TopBox>
      <Liner></Liner>
      <CommentsCounts></CommentsCounts>

      <ReplyCard
        title="The first title"
        at="1day ago"
        paragraph="Tempore dolorum unde? Asperiores, repellendus ad"
      ></ReplyCard>

      <ReplyCard
        title="another title"
        at="1minute ago"
        paragraph="Tempore dolorum unde? Asperiores, repellendus ad"
      ></ReplyCard>
      <ReplyCard
        title="Good Title"
        at="1yr ago"
        paragraph="Tempore dolorum unde? Asperiores, repellendus ad"
      ></ReplyCard>
      <ReplyCard
        title="I love vue"
        at="1minute ago"
        paragraph="Tempore dolorum unde? Asperiores, repellendus ad"
      ></ReplyCard>
    </div>
  </div>
</template>

<script lang="ts" setup>
import TopBox from "./TopBox.vue";
import Liner from "./Liner.vue";
import CommentsCounts from "./CommentsCounts.vue";
import ReplyCard from "./ReplyCard.vue";
</script>
