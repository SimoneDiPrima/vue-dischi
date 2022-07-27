<template>
    <header class="d-flex justify-content-between align-items-center">
 <i class="fa-brands fa-spotify icon-header"></i>
 <select class="me-3 mt-3 form-select select-menu" name="" id="">
  <option value="">rock</option>
  <option value="">pop</option>
  <option value="">metal</option>
  <option value="">punk</option>
 </select>
    </header>

</template>


<script>

export default {
  name:'HeaderLogo',
  
}

</script>

<style lang="scss">
@import '../assets/scss/vars';
header{
  min-height:200px;
 background-color:$Primary_color;
}
.icon-header{
  font-size: 2rem;
  color:$Logo_Color ;
 margin:20px;
}
.select-menu{
  max-width:10rem;
  height:2rem;
}

</style>