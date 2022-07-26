<template>
<div class="diskArticle text-center mb-2">
    <img :src="image" :alt="nameAlbum" class="img-fluid mb-3 p-2">
    <h4 class="text-white text-uppercase ">{{ nameAlbum }}</h4>
    <h5 class="author"> {{ author }}</h5>
    <h6 class="year">{{ year }}</h6>
</div>

</template>

<script> 

export default {
 name: 'SingleDisk',
 props:{
    nameAlbum : String,
    image : String,
    author : String,
    year : String
 }
}


</script>

<style lang="scss" scoped>
@import '../assets/scss/vars';
 .diskArticle{
    background-color:  $Primary_color;
    min-width:100%;
    margin:-10px;
 }
 .author,.year{
    color: $Name_author;
 }
</style>