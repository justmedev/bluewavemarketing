<template>
  <nav>
    <div style="display: flex; align-items: center">
      <div>
        <img src="../assets/logo.webp" alt="Bluewave marketing logo"
             style="background: #f9f9f9; border-radius: 3px; height: 40px"/>
      </div>
      <template v-if="!useMobileNav">
        <a :href="item.target" v-for="item in navItems">{{ item.title }}</a>
      </template>
    </div>

    <div class="right">
      <a href="mailto:boehm@bluewavemarketing.at?subject=Kontaktaufnahme%20via%20Web" v-if="!useMobileNav">
        Contact Us
      </a>
      <button v-else @click="showMobileNav = !showMobileNav">
        <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="white" height="24" style="margin-right: 0">
          <path d="M3,6H21V8H3V6M3,11H21V13H3V11M3,16H21V18H3V16Z"/>
        </svg>
      </button>
    </div>
  </nav>

<Transition>
  <div
      style="z-index: 1000; background: rgba(0,0,0,.5); position: absolute; width: 100%; height: 100%; display: flex; justify-content: center; align-items: center"
      v-if="showMobileNav" @click="showMobileNav = false">
    <div class="card">
      <button class="block" style="margin-bottom: 2px;" v-for="item in navItems" :href="item.target">{{ item.title }}</button>
    </div>
  </div>
</Transition>
</template>

<script setup lang="ts">
import { onMounted, onUnmounted, ref } from "vue";

const useMobileNav = ref(false);
const showMobileNav = ref(false);

const navItems = [
  {
    title: 'About',
    target: '#about',
  },
  {
    title: 'Knowledge',
    target: '#knowledge',
  },
  {
    title: 'Projects',
    target: '#projects',
  },
];

onMounted(onResize);
window.addEventListener('resize', onResize);
onUnmounted(() => {
  window.removeEventListener('resize', onResize);
});

function onResize() {
  useMobileNav.value = window.innerWidth < 1000;
}
</script>

<style scoped lang="scss">
$navbarBack: #222;
$onNav: #fff;

nav {
  user-select: none;
  background: $navbarBack;
  color: $onNav;
  padding: 18px;
  font-size: 18px;

  display: flex;
  align-items: center;
  justify-content: space-between;

  :first-child {
    display: flex;
    flex-direction: row;

    :first-child {
      font-weight: bold;
      margin-right: 2em;
    }

    > div, a {
      color: white;
      text-decoration: none;
      margin-right: 30px;
      font-weight: 500;
      cursor: pointer;

      &:not(:first-child) {
        &::after {
          content: "";
          margin-left: 1.4em;
          height: 2px;
          background-color: white;
          display: block;
          width: 0;
          transition: width 300ms;
        }

        &:not(:nth-child(2)):hover::after {
          width: calc(100% - 1.4em);
        }

        &:nth-child(2) {
          &:hover::after {
            width: 100%;
          }

          &::after {
            margin-left: 0;
          }
        }

        &:not(:nth-child(2))::before {
          margin-right: 1em;
          content: '/';
          color: rgba(255, 255, 255, 0.5);
        }
      }
    }
  }

  > .right > a {
    cursor: pointer;
    display: block;
    color: $onNav;
    text-decoration: none;

    &:hover::before {
      display: block;
      white-space: nowrap;
      overflow: hidden;
      position: absolute;

      content: "Contact Us";
      color: $navbarBack;
      background: $onNav;

      max-width: fit-content;

      -webkit-animation: widthZeroToFull 200ms ease-in-out 1;
      -o-animation: widthZeroToFull 200ms ease-in-out 1;
      animation: widthZeroToFull 200ms ease-in-out 1;
      animation-iteration-count: 1;
      animation-fill-mode: forwards;
    }
  }
}

@keyframes widthZeroToFull {
  from {
    width: 0;
  }

  to {
    width: 6rem;
  }
}

.v-enter-active,
.v-leave-active {
  transition: opacity 0.15s ease;
}

.v-enter-from,
.v-leave-to {
  opacity: 0;
}
</style>
