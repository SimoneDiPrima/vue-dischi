<template>
<div>
  <HeaderLogo/>
   <MainDisks/>
 
</div>

</template>

<script>
import HeaderLogo from './components/HeaderLogo.vue'
import MainDisks from './components/MainDisks.vue'

export default {
  components:{
    HeaderLogo,
    MainDisks,
}
}
</script>

<style lang="scss">
@import './assets/scss/style.scss';

</style>
