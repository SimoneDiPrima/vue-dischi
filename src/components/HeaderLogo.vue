<template>
    <header>
 <i class="fa-brands fa-spotify icon-header "></i>
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
 background-color:$Primary_color;
}
.icon-header{
  font-size: 2rem;
  color:$Logo_Color ;
 margin:20px;
}

</style>