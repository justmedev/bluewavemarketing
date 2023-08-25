<template>
  <div style="width: 100%; display: flex; justify-content: center; margin-top: 16px;" ref="logo">
    <img src="../assets/logo.webp" class="logo" alt="BlueWave Logo"/>
  </div>

<section id="about">
  <h1>
    About us
  </h1>
  <div>
    Test
  </div>
</section>
</template>

<script setup lang="ts">

</script>

<style scoped>
.logo {
  width: 40%;
  transition: width 250ms ease-in-out;
}

@media only screen and (max-width: 850px) {
  .logo {
    margin-top: 10px;
    width: 60%;
  }
}

@media only screen and (max-width: 600px) {
  .logo {
    margin-top: 10px;
    width: 70%;
  }
}
</style>
