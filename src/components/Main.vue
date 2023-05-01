
<script>
import Cards from './Cards.vue'

export default {
    name: 'Main',
    components:{
      Cards
    }
}
</script>

<template>
  <main>
    <div class="jumbotron">
     
    </div>
    <div class="main-wrapper">
      <div class="container">
        <h2>CURRENT SERIES</h2>
        
        <Cards/>
      </div>
    </div>
  </main>
</template>

<style lang="scss" scoped>
@use '../scss/variables' as *;
  
    .jumbotron{
      background-image: url(../assets/img/jumbotron.jpg);
      background-size: cover;
      background-repeat: no-repeat;
      height: 300px;
      width: 100%;
    }
    
    .main-wrapper{
        background-color: #1C1C1C;
        height: 95vh;
      .container{
        position: relative;

          h2{
            color: $color_white;
            background-color:  $color_blue;
            padding: 10px 15px;
            position: absolute;
            top: -30px;
            cursor: pointer;
          }
      }
    }
</style>