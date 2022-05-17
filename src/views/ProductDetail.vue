<template>
  <div class="product-detail">
    <Navbar />
    <div class="container">
      <div class="row mt-5">
        <div class="col">
            <nav aria-label="breadcrumb">
            <ol class="breadcrumb">
                <li class="breadcrumb-item">
                    <router-link to="/" class="text-dark">Home</router-link>
                </li>
                <li class="breadcrumb-item">
                    <router-link to="/product" class="text-dark">Product</router-link>
                </li>
                <li class="breadcrumb-item active" aria-current="page">Product Spesification
                </li>
            </ol></nav>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Navbar from "@/components/Navbar.vue";

export default {
  name: "ProductDetail",
  components: {
    Navbar,
  },
};
</script>