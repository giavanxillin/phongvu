<template>
  <div class="home">
    <Header />
    <Navbar id="navbar"/>
    <Carousel/>
    <Product/>
    <TopSale/>
    <Laptop/>
    <Footer style="margin-top: 50px;"/>
  </div>
</template>

<script>
// @ is an alias to /src
import Header from '@/components/Header.vue'
import Navbar from '../components/Navbar'
import Carousel from '../components/Carousel'
import TopSale from '../components/TopSale'
import Laptop from '../components/Laptop'
import Footer from '../components/Footer'
import Product from '../components/Product.vue'
export default {
  name: 'Home',
  components: {
    Header,
    Navbar,
    Carousel,
    Product,
    TopSale,
    Laptop,
    Footer
  },

  mounted(){
  window.document.onscroll = () => {
      let navbar = document.getElementById('navbar');
      if(window.pageYOffset > navbar.offsetTop){
        navbar.classList.add('sticky')
        } else {
        navbar.classList.remove('sticky')
      }
    }
  }
}
</script>
<style scoped>
.sticky {
  position: fixed;
  top: 0;
  width: 100%;
  z-index: 1000;
}

</style>
