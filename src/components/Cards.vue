<script>
import films from '../data/dc-comics.json'
export default {
    name: 'Cards',
    data(){
      return{
        films,
      }
    },
    props:{
      thumb: String,
      series: String
    }
}
</script>

<template>

  
    <!-- Cicled div card -->
    <div class="card">

      <img :src="thumb">

      <div class="title-card">
        <a href="#">{{ series.toUpperCase() }}</a>
      </div>
    </div>
  

  
</template>

<style lang="scss" scoped>
@use '../scss/variables' as *;

  
  
    // Cards style
  .card{
    width: calc(100% / 6);
    padding: 50px 20px 0 20px;

    img{
      width: 100%;
      height: 170px;
    }

    .title-card{
      padding-top: 15px;

      a{
      color: $color_white;
      font-size: 14px;

      &:hover{
        text-decoration: underline;
      }
      }
    }
  }


</style>