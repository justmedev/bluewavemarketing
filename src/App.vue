<script setup lang="ts">
import Navbar from "./components/Navbar.vue";
import Home from "./views/Home.vue";
</script>

<template>
  <Navbar/>
  <main class="container">
    <div>
      <Home/>
    </div>
  </main>
  <footer>
    <div>
      <div>
        &copy; bluewavemarketing.at 2023 - present &ctdot; All rights reserved
      </div>
      <div>

      </div>
    </div>
  </footer>
</template>

<style scoped lang="scss">
footer {
  user-select: none;
  position: absolute;
  bottom: 0;
  width: 100%;
  background: #1a1a1a;
  color: #c2c2c2;
  display: flex;
  flex-direction: row;
  justify-content: space-between;

  > div {
    margin: 5px 10px;
  }
}

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
