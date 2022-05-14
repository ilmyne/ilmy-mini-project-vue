<template>
  <div class="home">
    <Navbar />
    <div class="container">
    <Hero3 />

    </div>
  </div>
</template>

<script>
// @ is an alias to /src
import Navbar from '@/components/Navbar.vue'
import Hero3 from '@/components/Hero3.vue'

export default {
  name: 'AboutView',
  components: {
    Navbar,
    Hero3
}
}
</script>
