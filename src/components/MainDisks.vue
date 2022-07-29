<template>
  <main id="MainDisks">
    <div class="container offset-1 col-10 ">
      <div class="Disks-list row py-5 gy-3">
        <div class="singleDisk col-lg-2 text-center col-md-3 col-sm-6 col-xs-12 d-flex flex-wrap" v-for="disk in filteredDisks"
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
    return {disks : []}
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
    axios.get('https://flynn.boolean.careers/exercises/api/array/music').then((res)=>{
      this.disks = res.data.response
      })
  },
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