<template>
<div id="app"> 
  <div
    class="
      justify-center
      inline-block
      align-middle
      h-full
      rounded-sm
      bg-shark
      w-1/1
      mt-1
      my-5
    "
  >
    <img class="rounded-full" alt="Vue logo" src="../assets/logo.png" />
    <div class="text-white">
      <home-debricked msg="" />
      
    </div>
  </div>
  </div>
</template>

<script>
// @ is an alias to /src
import HomeDebricked from "@/components/HomeDebricked.vue";

export default {
  name: "Home",
  components: {
   HomeDebricked,
  },
};
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #090e14;
  background: rgb(10, 10, 10);
  padding: 30px;
  color: rgb(241, 233, 233);

  a {
    font-weight: bold;
    color: #8262d3e3;

    &.router-link-exact-active {
      color: #f5f8f7;
    }
  }
}
</style>

