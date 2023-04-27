
<script>
import Header from './components/Header.vue'
import Main from './components/Main.vue'
import Options from './components/Options.vue'
import Footer from './components/Footer.vue'

export default {
  name: 'App',
  components:{
    Header,
    Main,
    Options,
    Footer
  }
}
</script>

<template>
  <div class="main-wrapper">
    
      <Header/>
      <Main/>
      <Options/>
      <Footer/>
    
  </div>
</template>

<style lang="scss">
  @use './scss/main.scss'
</style>