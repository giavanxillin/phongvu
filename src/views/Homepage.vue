<template>
  <div class="home">
    <Header/>
    <Navbar/>
  </div>
</template>

<script>
// @ is an alias to /src
import Header from '@/components/Header.vue'
import Navbar from '../components/Navbar'

export default {
  name: 'Home',
  components: {
    Header,
    Navbar
  }
}
</script>
