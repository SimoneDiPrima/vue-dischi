<template>
<div>
  <header>
 <i class="fa-brands fa-spotify icon-header"></i>
 </header>
 <main>
  <div class="container">
    <div class="row">
      <div class="offset-1 col-10 allDisks">

      </div>
    </div>
  </div>

 </main>

</div>

</template>

<script>


export default {
  
}
</script>

<style lang="scss">
@import './assets/scss/style.scss';
header{
  background-color: #2E3A46;
}
main{
  height:100vh;
  background-color: #1E2D3B;
}
.allDisks{
  border:1px solid red;
  height:100vh;
}
.icon-header{
  font-size: 80px;
  color:green;
 margin:10px;
}
</style>
