<template lang="">
    <form @submit.prevent class='form'>
        <label class="styled-label">Your Name <styled-input name='name' v-model='comment.name' placeholder='enter some name' type="text"/></label>
        <label class="styled-label">Your  Email <styled-input name='email' v-model='comment.email' placeholder='enter some email' type="email"/></label>
        <label class="styled-label">Your Comment <styled-input  name='comment' v-model='comment.text' placeholder='enter some comment' type="text"/></label>
<styled-button @click='createComment' type="submit">Create</styled-button>
    </form>
</template>
<script>

export default {
    // name: 'CommentForm',
    data(){
        return { 
        comment: {
            name: '',
            email: '',
            text: ''
        }
        }
    },methods:{
        createComment(){  

this.comment.id = Date.now()
this.$emit('create',this.comment)
console.log(this.comment
);
    // this.name = ''
    //  this.email = ''
    //  this.text = ''
        
    },

    }

}
</script>
<style scoped
 >

    .form{
        display: flex;
        align-items:flex-end;
        /* flex-direction: column; */
        gap: 10px;
        /* background-color: ; */
    } 
    .styled-label{
    display: flex; 
    flex-direction: column;

 }
</style>