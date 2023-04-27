
<script>
import {headerMenu} from '../data/database.js'
export default {
    name: 'Header',
    data(){
        return{
            headerMenu,
        }
    }
}
</script>

<template>
  <header>
    <div class="container">
        <div class="header-container d-flex-space-bet">
        <div class="image">
            <img src="../assets/img/dc-logo.png" alt="dc-logo">
        </div>
        <div class="h-link d-flex-cont-center-items-center">
            <nav>
                <ul class="d-flex">
                    <!-- <li ><a class="active" href="#">CHARACTERS</a></li>
                    <li><a href="#">COMICS</a></li>
                    <li><a href="#">MOVIES</a></li>
                    <li><a href="#">TV</a></li>
                    <li><a href="#">GAMES</a></li>
                    <li><a href="#">COLLECTIBLES</a></li>
                    <li><a href="#">VIDEOS</a></li>
                    <li><a href="#">FANS</a></li>
                    <li><a href="#">NEWS</a></li>
                    <li><a href="#">SHOP</a></li> -->
                    <li v-for="(link, index) in headerMenu" :key="index" ><a :class="{ 'active' : link.isActive}" href="#">{{ link.text }}</a></li>
                </ul>
            </nav>
        </div>
    </div>
    </div>
  </header>
</template>

<style lang="scss" scoped>
@use '../scss/variables' as *;
    header{
        height: 100px;
    }

    .header-container{
        height: 100%;
    }
    .image{
        img{
            height: 70px;
            width: 70px;
            object-fit: cover;
        }
    }
    
    .h-link{
        height: 100%;
        
        ul{
            height: 100%;
        }
        
        li{
            height: 100%;
            padding: 0 15px;
        }

        a{
            font-weight: bold;
        }
    }

</style>