<template lang="">
    <input class="styled-input" :name='name' :value='value' type='text'/>
        
</template>
<script>
export default {
    name:"styled-input",
    props:{
        name: {type:String,required: true},
        modelValue: [String, Number]
    },
    methods: {
        updateInput(e){
this.$emit('update:modelValue', e.target.value)
        }
    }
}
</script>
<style scoped>
    .styled-input{
        padding: 10px;
        margin: 5px;
    }
</style>