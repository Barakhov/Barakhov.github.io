<template>
  <div id="app">
    <nav>
      <router-link to="/">Home</router-link>
      <span style="padding: 0 5px">|</span>
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
  text-align: center;

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
