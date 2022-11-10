<template>
  <div id="app">
    <nav class="header_nav">
      <router-link class="nav_router_link" to="/">Пошук героя</router-link><span class="nav_border"> | </span>
      <router-link class="nav_router_link" to="/Intergalactic_TV">Міжгалактичне ТВ</router-link><span class="nav_border"> | </span>
      <!-- <router-link to="/in_memory">Речі на пам'ять</router-link> |  -->
      <a class="nav_router_link" href="https://rozetka.com.ua/search/?text=%D1%80%D1%96%D0%BA+%D1%96+%D0%BC%D0%BE%D1%80%D1%82%D1%96">Речі на пам'ять</a>
    </nav>
    <router-view/>
  </div>
</template>

<style lang="scss" src="./assets/styles/index.scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  position: relative;
}

nav {
  a {
    font-weight: bold;
    color: #2c3e50;

    &.router-link-exact-active {
      color: #42b983;
    }
  }
}
</style>
