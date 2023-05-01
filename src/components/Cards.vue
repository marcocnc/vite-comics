<script>
import films from '../data/dc-comics.json'
export default {
    name: 'Cards',
    data(){
      return{
        films,
      }
    }
}
</script>

<template>
  <div class="card-wrapper d-flex">
    <div class="card" v-for="(film, index) in films" :key="index">
      <img :src="film.thumb">
      <div class="title-card">
        <a href="#">{{ film.series.toUpperCase() }}</a>
      </div>
    </div>
  </div>

  <div id="load-more" class="d-flex-cont-center-items-center">
    <span>LOAD MORE</span>
  </div>
</template>

<style lang="scss" scoped>
@use '../scss/variables' as *;

  .card-wrapper{
    flex-wrap: wrap;
  
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

  }
  #load-more{
    span{
      margin-top: 40px;
      background-color: $color_blue;
      color: $color_white;
      padding: 10px 45px;
      cursor: pointer;
    }
  }


</style>