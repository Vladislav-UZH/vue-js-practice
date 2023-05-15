<template lang="">
  <div class="list">
    <comment-item v-for="comment in comments" :key="comment.id"  @delete="$emit('delete',id)" :comment='comment' />
  </div>
</template>
<script>
import CommentItem from "@/components/CommentItem";

export default {
  // name: "CommentsList",
  components: {CommentItem},
  props: {
    delete: { type: Function},
    comments: {type: [], required:true}
  }
};
</script>
<style scoped>
.list{display: flex;
flex-direction: column;
gap: 10px;}
</style>
