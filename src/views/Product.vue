<template>
  <div class="product">
    <Navbar />
    <div class="container">
      <Hero2 />
      <!-- <div class="d-flex h-100">
      <div class="justify-content-center align-self-center">
        <b-dropdown
          text="Choose your preference"
          id="dropdown-left"
          variant="primary"
          class="float-right"
        >
          <b-dropdown-item href="#">ASUS</b-dropdown-item>
          <b-dropdown-item href="#">Lenovo</b-dropdown-item>
          <b-dropdown-item href="#">Samsung</b-dropdown-item>
        </b-dropdown>
      </div>
    </div> -->
    </div>
  </div>
</template>

<script>
// @ is an alias to /src
import Navbar from "@/components/Navbar.vue";
import Hero2 from "@/components/Hero2.vue";

export default {
  name: "Product",
  components: {
    Navbar,
    Hero2,
  },
};
</script>

<style>
</style>