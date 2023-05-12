<template lang="">
  <div class='item'>
    <p><strong>Name:</strong> <span>{{ comment.name }}</span></p>
    <p><strong>Email:</strong> <span>{{ comment.email }}</span></p>
    <p> <strong>Comment:</strong> <span>{{ comment.body }}</span></p>
  </div>
</template>
<script>
export default {
  props: {
    comment: {
      type: Object,
      required: true,
    },
  },

  // data(){
  //     return{

  //     }
  // }
};
</script>
<style scoped>
.item{
    border: #ccc solid 1px;
    padding: 10px;
}
</style>
