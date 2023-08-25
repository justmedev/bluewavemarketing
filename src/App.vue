<script setup lang="ts">
import Navbar from "./components/Navbar.vue";
import Home from "./views/Home.vue";
</script>

<template style="height: 100vh">
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
  display: flex;
  justify-content: center;

  > div {
    width: 70%;
  }
}
</style>
