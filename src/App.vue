<template>
<div>
  <HeaderLogo  @gen-options="genMenu"   />
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
},
methods:{
 genMenu() {
  console.log(`mi hanno cliccato`)
 }
},

}
</script>

<style lang="scss">
@import './assets/scss/style.scss';

</style>
