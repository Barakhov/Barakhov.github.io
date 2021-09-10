<template>
  <div id="app">
    <div class="main-grid">
      <header class="header">
        <div class="container">
          <div class="d-f ai-c jc-sb h100">
            <Logo />
            <nav>
              <router-link to="/">Home</router-link>
              <span style="padding: 0 5px">|</span>
              <router-link to="/about">About</router-link>
            </nav>
          </div>
        </div>
      </header>
      <main class="main">
        <div class="container">
          <transition name="fade" mode="out-in">
            <router-view />
          </transition>
        </div>
      </main>
      <footer class="footer">
        <div class="container">footer</div>
      </footer>
    </div>
  </div>
</template>

<script>
// @ is an alias to /src
import Logo from "@/components/Logo.vue";

export default {
  name: "App",
  components: {
    Logo,
  },
};
</script>

<style lang="scss">
#app {
  color: $clr-black;
}

nav {
  a {
    color: $clr-black;
    text-decoration: none;

    &:hover,
    &.router-link-exact-active {
      color: $clr-primary;
      text-decoration: underline;
    }
  }
}

.fade-enter-active,
.fade-leave-active {
  transition: opacity 0.25s;
}

.fade-enter,
.fade-leave-to {
  opacity: 0;
}
</style>
