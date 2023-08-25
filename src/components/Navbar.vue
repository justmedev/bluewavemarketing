<script setup lang="ts">

</script>

<template>
  <nav>
    <div>
      <div>
        <img src="../assets/logo.webp" height="28px" alt="Bluewave marketing logo"
             style="background: #f9f9f9; border-radius: 3px"/>
      </div>
      <a href="#about">About</a>
      <a href="#knowledge">Knowledge</a>
      <a href="#projects">Projects</a>
    </div>

    <div class="right">
      <a href="mailto:boehm@bluewavemarketing.at?subject=Kontaktaufnahme%20via%20Web">Contact Us</a>
    </div>
  </nav>
</template>

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
</style>
