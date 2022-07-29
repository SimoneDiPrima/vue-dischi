<template>
  <div>
    <HeaderLogo :music-list="musicList" @genre-change="setSelectedGenre " />
    <MainDisks :select-genre="selectedGenre" />
  
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
       data() {
      return {
      musicList : ['Rock','Metal','Pop','Jazz'],
      selectedGenre : ''
      }
    },
     methods:{
      setSelectedGenre(newGen){
         this.selectedGenre = newGen;
      }
  
    }
  }
</script>

<style lang="scss">
@import './assets/scss/style.scss';

</style>
