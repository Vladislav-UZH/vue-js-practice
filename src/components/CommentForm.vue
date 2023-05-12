<template lang="">
    <form @submit.prevent='handleSubmit' class='form'>
        <label >Your Name<input name='name' placeholder='enter some name' type="text"></label>

        <label >Your  Email<input name='email' placeholder='enter some email' type="email"></label>
        <label >Your Comment<input  name='comment' placeholder='enter some comment' type="text"></label>
<button type="submit">Create</button>
    </form>
</template>
<script>
export default {
    // name: 'CommentForm',
    data(){
        return { 
            value:null
        }
    },methods:{
        handleSubmit(e){
            // e.preventDefault();
         const {value}=   e.target.elements.name
         alert(value)
        
    }
    }

}
</script>
<style scoped
 lang="">
    /* form{
        background-color: black;
    } */
</style>