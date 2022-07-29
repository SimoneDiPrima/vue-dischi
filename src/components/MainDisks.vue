<template>
  <main id="MainDisks">
    <div class="container offset-1 col-10 ">
      <div class="Disks-list row gy-3 py-3">
        <div class="singleDisk col-lg-2 d-flex flex-wrap" v-for="disk in filteredDisks"
          :key="disk.title">
          <SingleDisk :image="disk.poster"
            :nameAlbum="disk.title" 
            :author="disk.author"
            :year="disk.year"
            :genre="disk.genre" role="button"/>
        </div>

      </div>

    </div>
    
  </main>

</template>

<script> 
import axios from 'axios';
import SingleDisk from './SingleDisk.vue';

export default {
  name:'MainDisks',
  data(){
    return {disks : [],
     }
  },
  props:{
    selectGenre : String
  },
  computed:{
    filteredDisks(){
       if(!this.selectGenre) return this.disks;
     return this.disks.filter((disk) => {
      if(disk.genre == this.selectGenre) return true;

      })
    }
  },
  created(){
    axios.get('https://flynn.boolean.careers/exercises/api/array/music')
    .then((res)=>{
      this.disks = res.data.response
      const genres = [ ]
      this.disks.forEach((disk) => {
        if(!genres.includes(disk.genre))genres.push(disk.genre)
      })
      this.$emit('fetch-disks',genres) } )
      }
  ,
  components:{ SingleDisk },
}


</script>

<style lang="scss" scoped>
  @import '../assets/scss/vars';
  #MainDisks{
    background-color:$Secondary_color;
  }
  .singleDisk{ flex-basis:20%;}
</style>