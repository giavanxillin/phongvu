<template>
  <div class="home">
    <Header />
    <Navbar id="navbar"/>
    <Carousel/>
  </div>
</template>

<script>
// @ is an alias to /src
import Header from '@/components/Header.vue'
import Navbar from '../components/Navbar'
import Carousel from '../components/Carousel'

export default {
  name: 'Home',
  components: {
    Header,
    Navbar,
    Carousel
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
  width: 100%
}

</style>