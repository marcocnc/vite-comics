
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

            <!-- Logo -->
        <div class="image">
            <img src="../assets/img/dc-logo.png" alt="dc-logo">
        </div>
        
            <!-- Links -->
        <div class="h-link d-flex-cont-center-items-center">
            <nav>
                <ul class="d-flex">
                    <li v-for="(link, index) in headerMenu" :key="index">
                        <a :class="{ 'active' : link.isActive}" href="#">{{ link.text }}</a>
                    </li>
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

    // Image
    .image{
        img{
            height: 70px;
            width: 70px;
            object-fit: cover;
        }
    }
    
    // Links style
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