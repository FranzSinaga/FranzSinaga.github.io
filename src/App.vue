<template>
  <div id="app">
    <div class="container">
<!--      <Navbar/>-->
    </div>
    <Home/>
    <Footer/>
  </div>
</template>

<script>
import Navbar from './components/Navbar.vue'
import Footer from './components/Footer.vue'
import Home from './views/Home.vue'

export default {
  name: 'app',
  components: {
    Navbar,
    Footer,
    Home,
  }
}
</script>

<style>
  html{
    scroll-behavior: smooth;
  }
  #app {
    font-family: 'Avenir', Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2c3e50;
    margin-top: 60px;
}
</style>
