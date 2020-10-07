<template>
  <Header />
  <Hero />
  <ProductGroup />
  <FeaturedProducts />
  <CTA />
  <Testimonials />
  <Footer />
</template>

<script>
import Header from './components/Header.vue'
import Hero from './components/Hero.vue'
import ProductGroup from './components/ProductGroup.vue'
import FeaturedProducts from './components/FeaturedProducts.vue'
import CTA from './components/CallToAction.vue'
import Testimonials from './components/Testimonials.vue'
import Footer from './components/Footer.vue'

export default {
  name: 'App',
  components: {
    Header,
    Hero,
    ProductGroup,
    FeaturedProducts,
    CTA,
    Testimonials,
    Footer
  }
}
</script>

<style lang="scss">
button{
  transition: .35s;
  &:hover{
    background-color: white !important;
    color: #ff6d33 !important;
    border-color: #ff6d33 !important;
  }
}
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
