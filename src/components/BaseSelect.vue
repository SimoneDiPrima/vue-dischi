<template>
<select class="me-3 mt-3 form-select select-menu" name="" id="">
    <option v-for="option in options" :key="option.title">
        {{ option }}
    </option>
</select>

</template>

<script> 

export default {
 name: 'BaseSelect',
 data(){
    return{
        options:[`rock`,`metal`,`pop`,`punk`]
    }
 },
 props:{
    genre:String
 }
}

</script>

<style lang="scss" scoped>
 .select-menu{
  max-width:10rem;
  height:2rem;
}
</style>