
<script>
export default {
    name: 'Footer'
}
</script>

<template>
  <footer>
    <div class="footer-top">
        <div class="container d-flex h-100">
            <div class="footer-nav ">
                <h1>testo</h1>
            </div>
            <div class="dc-logo-footer">
                <h1>testo</h1>
            </div>
        </div>
    </div>
    <div class="footer-bottom">
        <div class="container">
            <h1>testo</h1>
        </div>
    </div>
  </footer>
</template>

<style lang="scss" scoped>
    footer{
        height: 70%;
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
            background-color: #981d1d;
        }

        .dc-logo-footer{
            background-color: #90981d;
        }
    }
    .footer-bottom{
        height: 30%;
        background-color: #303030;
    }
</style>