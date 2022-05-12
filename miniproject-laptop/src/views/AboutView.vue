<template>
  <div class="home">
    <Navbar />
    <div class="container">
    <Hero />
    <div class="footer">
    <Footer />
    </div>

    </div>
  </div>
</template>

<script>
// @ is an alias to /src
import Navbar from '@/components/Navbar.vue'
import Hero from '@/components/Hero.vue'
import Footer from '@/components/Footer.vue'

export default {
  name: 'AboutView',
  components: {
    Navbar,
    Hero,
    Footer
}
}
</script>
