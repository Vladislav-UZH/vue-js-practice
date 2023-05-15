<template lang="">
    <button class='styled-button'>
        <slot>Create</slot>
    </button>
</template>
<script>
export default {
    name:'styled-button'
}
</script>
<style scoped>
    .styled-button{  
        width: 90px;
        height: 40px;
        margin: 5px;
        /* padding: 10px 20px; */
        background-color: transparent;
        border: #ccc solid 1px;
    }
    .styled-button:hover{
      
        background-color: #ccc;
    }
</style>