<template lang="">
  <div class='item'>
    <div>
    <p><strong>Name:</strong> <span>{{ comment.name }}</span></p>
    <p><strong>Email:</strong> <span>{{ comment.email }}</span></p>
    <p> <strong>Comment:</strong> <span>{{ comment.body }}</span></p></div>
    <styled-button @click='deleteComment' type='button'>Remove</styled-button>
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
  methods:{
    deleteComment(){
      console.log(this.delete);
const id = this.comment.id
this.$emit('delete', id)
    }
  }
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
