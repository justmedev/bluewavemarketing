<script setup lang="ts">
import Navbar from "./components/Navbar.vue";
import Home from "./views/Home.vue";

function openInstagram() {
  window.open("https://instagram.com/bluewavemarketing.at", "_blank");
}
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
        &copy; bluewavemarketing.at 2023 - present
        <div class="ctdot">&ctdot;</div>
        <div>
          All rights reserved
        </div>
      </div>
      <div class="instagram">
        <img src="./assets/instagram.svg" alt="Folge uns auf Instagram" @click="openInstagram"/>
        <a href="https://instagram.com/bluewavemarketing.at" target="_blank">
          @bluewavemarketing.at
        </a>
      </div>
    </div>
  </footer>
</template>

<style scoped lang="scss">
.instagram {
  display: flex;
  align-items: center;

  > img {
    cursor: pointer;
    width: 20px;
    margin-right: 5px;
  }

  > a {
    color: #c2c2c2 !important;
    transition: all 200ms ease-in-out;

    &:hover {
      color: #fff !important;
    }
  }
}

footer {
  user-select: none;
  position: absolute;
  bottom: 0;
  width: 100%;
  background: #1a1a1a;
  color: #c2c2c2;

  > :first-child {
    > div {
      display: flex;
      flex-direction: row;
      align-items: center;
    }
  }

  .ctdot {
    margin: 10px;
  }

  > div {
    margin: 5px 10px;

    display: flex;
    flex-direction: row;
    justify-content: space-between;
    flex-wrap: nowrap;
    align-items: center;
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

@media only screen and (max-width: 720px) {

footer {
  padding: 20px 5px;

  > div {
    text-align: center;
    flex-direction: column !important;

    > :first-child {
      margin-bottom: 5px !important;
      flex-direction: column;
    }
  }
}

.ctdot {
  display: none;
}
}
</style>
