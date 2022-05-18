<template>
<div>
  <b-navbar toggleable="lg" class="header" type="light" variant="light" fixed="top">
<div class="container">
    <b-navbar-brand href="/aboutview">
            <img src="../assets/img/logo.png" alt="" />
          </b-navbar-brand>

    <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>

    <b-collapse id="nav-collapse" is-nav>
      <b-navbar-nav>
        <li class="nav-item">
              <router-link class="nav-link" to="/">Home</router-link>
            </li>
            <li class="nav-item">
              <router-link class="nav-link" to="/product">Product</router-link>
            </li>
            <li class="nav-item">
              <router-link class="nav-link" to="/aboutview">About</router-link>
            </li>
      </b-navbar-nav>

      <!-- Right aligned nav items -->
      <b-navbar-nav class="ml-auto">

            <li class="nav-item">
              <router-link class="nav-link" to="/cart"
                >Cart
                <b-icon-cart></b-icon-cart>
                <span class="badge badge-success ml-2">{{ updateCart ? updateCart.length : quantity.length }}</span>
              </router-link>
            </li>
          
      </b-navbar-nav>
    </b-collapse>
</div>
  </b-navbar>
<hr />
<hr />
<hr />
</div>

  <!-- <nav class="navbar navbar-expand-lg navbar-light">
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
                <span class="badge badge-success ml-2">{{ updateCart ? updateCart.length : quantity.length }}</span>
              </router-link>
            </li>
          </ul>
        </div>
        </b-navbar>
      </div>
    </div>
    <hr />
  </nav> -->
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
  props: ['updateCart'],
  
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