<template>
  <div class="home">
    <Navbar />
    <div class="container">
      <Hero />

      <div class="row mt-4">
        <div class="col">
          <h2>Most Wanted</h2>
        </div>
        <div class="col">
          <router-link to="/product">
            <b-button variant="primary" size="lg" class="float-right"
              >More</b-button
            >
          </router-link>
        </div>
      </div>
      
      <div class="row mb-3">
        <div class="col-md-4 mt-4">
          <h2>Laptop</h2>
        </div>
      </div>

      <div class="footer">
      <Footer />
    </div>
    </div>
  </div>
</template>

<script>
// @ is an alias to /src
import Navbar from "@/components/Navbar.vue";
import Hero from "@/components/Hero.vue";
import Footer from "@/components/Footer.vue";

export default {
  name: "HomeView",
  components: {
    Navbar,
    Hero,
    Footer
},
};
</script>
