
<script>
import {footerMenuDcComics} from '../data/database.js';
import {footerMenuShop} from '../data/database.js';
import {footerMenuDc} from '../data/database.js';
import {footerMenuDcSites} from '../data/database.js';
export default {
    name: 'Footer',
    data(){
        return{
            footerMenuDcComics,
            footerMenuShop,
            footerMenuDc,
            footerMenuDcSites
        }
    }
}
</script>

<template>
  <footer>
    <div class="footer-top">
        <div class="container d-flex h-100">
            <div class="footer-nav d-flex">
                <div class="row">
                    <ul>
                        <li><h2>DC COMICS</h2></li>
                        <li v-for="(link, index) in footerMenuDcComics" :key="index">
                            <a :href="link.href">{{ link.text }}</a>
                        </li>
                    </ul>
                    <ul>
                        <li><h2>SHOP</h2></li>
                        <li v-for="(link, index) in footerMenuShop" :key="index">
                            <a :href="link.href">{{ link.text }}</a>
                        </li>
                    </ul>
                </div>
                <div class="row d-flex">

                    <ul>
                        <li><h2>DC</h2></li>
                        <li v-for="(link, index) in footerMenuDc" :key="index">
                            <a :href="link.href">{{ link.text }}</a>
                        </li>
                    </ul>

                    <ul>
                        <li><h2>SITES</h2></li>
                        <li v-for="(link, index) in footerMenuDcSites" :key="index">
                            <a :href="link.href">{{ link.text }}</a>
                        </li>
                    </ul>
                </div>
            </div>
            <div class="dc-logo-footer">
                <!-- <img src="../assets/img/dc-logo-bg.png" alt=""> -->
            </div>
        </div>
    </div>
    <div class="footer-bottom">
        <div class="container h-100 d-flex-space-bet">
            <div class="f-left">
                <button>SIGN-UP NOW!</button>
            </div>
            <div class="f-right d-flex align-center">
                
                    <h3>FOLLOW US</h3>
                    <img src="../assets/img/footer-facebook.png" alt="">
                    <img src="../assets/img/footer-twitter.png" alt="">
                    <img src="../assets/img/footer-youtube.png" alt="">
                    <img src="../assets/img/footer-pinterest.png" alt="">
                    <img src="../assets/img/footer-periscope.png" alt="">
                
            </div>
        </div>
    </div>
  </footer>
</template>

<style lang="scss" scoped>
@use '../scss/variables' as *;

    footer{
        height: 50%;
        background-image: url(../assets/img/footer-bg.jpg);
        background-size: cover;
    }

    .footer-top{
        height: 100%;

        .footer-nav,
        .dc-logo-footer{
            width: 50%;
            height: 100%;
        }

        .footer-nav{

            ul{
                padding: 40px 30px 5px 0;
            }

            h2{
                color: $color_white;
                padding-bottom: 10px;
            }

            a{
                font-size: 12px;
                color: $color_grey;

                &:hover{
                    text-decoration: underline;
                    color: $color_white;
                }
            }
        }

        .dc-logo-footer{
            background-image: url(../assets/img/dc-logo-bg.png);
            background-repeat: no-repeat;
            background-position-y: -90px;
        }
    }
    .footer-bottom{
        height: 30%;
        background-color: #303030;
    }

    .f-left{
        button{
            background-color: #303030;
            border: 1px solid $color_blue;
            color: $color_white;
            padding: 10px;
            font-weight: bold;
            font-size: 17px;
            cursor: pointer;

            &:active{
                background-color: $color_blue;
            }
        }
    }

    .f-right{

        h3{
            padding-right: 20px;
            color: $color_blue;

            &:hover{
                color: $color_white;
                cursor: pointer;
            }
        }

        img{
            object-fit: cover;
            vertical-align: middle;
            margin-right: 15px;
            cursor: pointer;
        }
    }
</style>