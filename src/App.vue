<template>
  <div class="text-1xl font-mono"  id="app">
    
    <router-link to="/">Home</router-link> |

    <router-link to="/upload">Services</router-link> |
    <router-link to="/contact">Contact</router-link> |
    <router-link to="/api"></router-link> 
    
    <router-view />
  </div>
  <div id="app"></div>
</template>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #090e14;
  background: rgb(10, 10, 10);
  color: rgb(241, 233, 233);
  padding: 30px;

  a {
    font-weight: bold;
    color: #8262d3e3;

    &.router-link-exact-active {
      color: #f5f8f7;
    }
  }
}
</style>
