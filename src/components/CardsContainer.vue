

<script>
import Cards from './Cards.vue';
import films from '../data/dc-comics.json'
export default {
    name:'CardsContainer',
    data(){
      return{
        films
      }
    },
    components:{
      Cards
    }
}
</script>

<template>

<div class="card-wrapper d-flex">

    <Cards v-for="(film, index) in films" :key="index"
        :thumb = film.thumb
        :series="film.series"
    />

      <!-- Button -->
  <div id="load-more" class="d-flex-cont-center-items-center">
    <span>LOAD MORE</span>
  </div>

</div>


</template>

<style lang="scss" scoped>
@use '../scss/variables' as *;
@use '../scss/utilities' as *;
.card-wrapper{
    flex-wrap: wrap;
}



// Button
#load-more{
    width: 100%;
    span{
      margin-top: 40px;
      background-color: $color_blue;
      color: $color_white;
      padding: 10px 45px;
      cursor: pointer;
    }
}
</style>