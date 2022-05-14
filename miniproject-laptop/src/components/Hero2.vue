<!-- /* eslint-disable vue/no-parsing-error */ -->
<template>
  <div class="row">
    <div class="col">
      <h2><strong>DevGear Product</strong></h2>

      <b-dropdown
          text="Choose your preference"
          id="dropdown-left"
          variant="primary"
          class="float-left"
        >
          <b-dropdown-item href="#">ASUS</b-dropdown-item>
          <b-dropdown-item href="#">Lenovo</b-dropdown-item>
          <b-dropdown-item href="#">Samsung</b-dropdown-item>
        </b-dropdown>

    </div>
  </div>
</template>

<script>
export default {
  name: "Hero2",
};
</script>

<style>
</style>