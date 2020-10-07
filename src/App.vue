<template>
  <Header />
  <Hero />
  <ProductGroup />
  <FeaturedProducts />
  <img alt="Vue logo" src="./assets/logo.png">
  <HelloWorld msg="Welcome to Your Vue.js App"/>
  <Footer />
</template>

<script>
import Header from './components/Header.vue'
import Hero from './components/Hero.vue'
import ProductGroup from './components/ProductGroup.vue'
import FeaturedProducts from './components/FeaturedProducts.vue'
import Footer from './components/Footer.vue'
import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'App',
  components: {
    HelloWorld,
    Header,
    Footer,
    Hero,
    ProductGroup,
    FeaturedProducts
  }
}
</script>

<style>
body{
  margin: 0;
}
#app {
  overflow: hidden;
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
</style>
