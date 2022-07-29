<template>
  <div>
    <HeaderLogo :music-list="musicList" @genre-change="setSelectedGenre " />
    <MainDisks :select-genre="selectedGenre" @fetch-disks ="setGenresList" />
  
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
      musicList:[ ],
      selectedGenre : ''
      }
    },
     methods:{
      setSelectedGenre(newGen){
         this.selectedGenre = newGen;
      },
      setGenresList(genres){
        this.musicList = genres
      }
  
    }
  }
</script>

<style lang="scss">
@import './assets/scss/style.scss';

</style>
