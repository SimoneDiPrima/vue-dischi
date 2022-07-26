<template>
<main id="MainDisks">
  <div class="container offset-1 col-10 ">
    <div class="Disks-list row py-3">
      <div class="col-2 m-1 d-flex flex-wrap" v-for="disk in disks"
        :key="disk.title">
       <SingleDisk :image="disk.poster" :nameAlbum="disk.title" :author="disk.author" :year="disk.year" />
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

</style>