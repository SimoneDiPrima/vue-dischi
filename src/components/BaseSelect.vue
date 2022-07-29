<template>
    <select class="me-3 mt-3 select-menu" v-model="selectedValue" @change="$emit('option-change',selectedValue)" name="" id="">
        <option value="">{{  selectedValue || `scegli un genere` }}</option>
        <option v-for="option in options" :key="option.value || option "
          :value="option.value || option ">{{ option.label || option }}</option>
    </select>
</template>

<script> 

    export default {
        name: 'BaseSelect',
        data(){
            return{
                selectedValue : ''
            }
        },
        props:{
            placeholder:String,
            options:Array

        },
        
    }

</script>

<style lang="scss" scoped>
    .select-menu{
        height:40px;
        }
 
</style>