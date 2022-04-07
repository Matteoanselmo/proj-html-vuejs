<template>
  <div id="app">
    <Header class="mb-2 bg-white"/>
    <Jumbotron class="bg-white"/>
    <Main/>
    <Footer/>
  </div>
</template>

<script>
import Header from './components/Header.vue'
import Jumbotron from './components/Jumbotron.vue'
import Main from './components/Main.vue'
import Footer from './components/Footer.vue'

export default {
  name: 'App',
  components: {
    Header,
    Jumbotron,
    Main,
    Footer
  }
}
</script>

<style lang="scss">
@import '@/style/main-style.scss';
@import '~@fortawesome/fontawesome-free/css/all.min.css';


</style>
