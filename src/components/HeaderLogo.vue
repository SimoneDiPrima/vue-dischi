<template>
    <header class="d-flex justify-content-between align-items-center">
 <i class="fa-brands fa-spotify icon-header"></i>
    <BaseSelect/>
    </header>

</template>


<script>
import BaseSelect from './BaseSelect.vue'

export default {
  name:'HeaderLogo',
  components:{ BaseSelect }
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
</style>