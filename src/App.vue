<template>
  <div id="app">
    <nav>
      <router-link to="/">Home</router-link> |
      <router-link to="/about">About</router-link>
    </nav>
    <main>
      <transition name="fade" mode="out-in">
        <router-view />
      </transition>
    </main>
  </div>
</template>

<style lang="scss">
#app {
  color: $clr-black;
}

nav {
  padding: 30px;

  a {
    color: $clr-black;
    text-decoration: none;

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
