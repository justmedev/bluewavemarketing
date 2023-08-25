<script setup lang="ts">
import Navbar from "./components/Navbar.vue";
import Home from "./views/Home.vue";
</script>

<template>
  <Navbar/>
  <div class="container">
    <div>
      <Home/>
    </div>
  </div>
</template>

<style scoped>
.container {
  width: 100vw;
  height: 100%;
  display: flex;
  justify-content: center;

  > div {
    width: 70%;
    transition: width ease-in-out 250ms;
  }
}

@media only screen and (max-width: 600px) {
  .container > div {
    width: 90% !important;
  }
}
</style>
