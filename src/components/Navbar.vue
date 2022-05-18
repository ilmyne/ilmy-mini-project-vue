<template>
  <nav class="navbar navbar-expand-lg navbar-light">
    <div class="container">
      <div class="container-fluid">
        <b-navbar class="header" type="light" variant="light" fixed="top">
          <b-navbar-brand href="/aboutview">
            <img src="../assets/img/logo.png" alt="" />
          </b-navbar-brand>
        <button
          class="navbar-toggler"
          type="button"
          data-bs-toggle="collapse"
          data-bs-target="#navbarSupportedContent"
          aria-controls="navbarSupportedContent"
          aria-expanded="false"
          aria-label="Toggle navigation"
        >
          <span class="navbar-toggler-icon"></span>
        </button>
        <div class="collapse navbar-collapse" id="navbarSupportedContent">
          <ul class="navbar-nav mr-auto">
            <li class="nav-item">
              <router-link class="nav-link" to="/">Home</router-link>
            </li>
            <li class="nav-item">
              <router-link class="nav-link" to="/product">Product</router-link>
            </li>
            <li class="nav-item">
              <router-link class="nav-link" to="/aboutview">About</router-link>
            </li>
          </ul>

          <ul class="navbar-nav ml-auto">
            <li class="nav-item">
              <router-link class="nav-link" to="/cart"
                >Cart
                <b-icon-cart></b-icon-cart>
                <span class="badge badge-success ml-2">{{ quantity.length }}</span>
              </router-link>
            </li>
          </ul>
        </div>
        </b-navbar>
      </div>
    </div>
    <hr />
  </nav>
</template>

<script>
import axios from "axios";

export default {
  name: "Navbar",

  data() {
    return {
      quantity: []
    }
  },
  
  methods: {
    setTotal(data) {
      this.quantity = data
    }
  },

  mounted() {
    axios
      .get(" http://localhost:3000/Cart")
      .then((response) => this.setTotal(response.data))
      .catch((error) => console.log(error));
  },
};
</script>

<style>
</style>