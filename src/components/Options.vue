<script>
import { ctaMenu } from '../data/database';
export default {
    name: 'Options',
    data(){
      return{
        ctaMenu,
      }
    },
    methods:{
        getImage(img){
            return new URL(img, import.meta.url).href;
        }
    }
}
</script>

<template>
  <section id="cta">
    <div class="container h-100">
        <div class="row d-flex-space-bet h-100">
            <div class="col d-flex-cont-center-items-center" v-for="(option, index) in ctaMenu" :key="index">
                <div class="cta-image">
                    <img :src="getImage(`../assets/img/${option.img}`)" alt="">
                </div>
                <div class="cta-text">
                    <span>{{ option.text }}</span>
                </div>
            </div>
        </div>
    </div>
  </section>
</template>

<style lang="scss" scoped>
@use '../scss/variables' as *;
    #cta{
        background-color: $color_blue;
        color: $color_white;
        height: 200px;
    }

    .cta-image{
        img{
            height: 70px;
            object-fit: cover;
            vertical-align: middle;
        }
    }

    .cta-text{
        span{
            padding-left: 10px;
            font-size: 14px;
        }
    }
</style>