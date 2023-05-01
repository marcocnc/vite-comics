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
    <div class="card">
      <img src="https://www.coverbrowser.com/image/action-comics/1-1.jpg" alt="">
      <div class="title-card">
        <a href="">TITOLO</a>
      </div>
    </div>
  </div>

  <div id="load-more" class="d-flex-cont-center-items-center">
    <button>bottone</button>
  </div>
</template>

<style lang="scss" scoped>
@use '../scss/variables' as *;

  .card-wrapper{
    flex-wrap: wrap;
  }
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
      font-size: 16px;
      }
    }
  }


</style>