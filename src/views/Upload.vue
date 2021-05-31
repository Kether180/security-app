<template>
  <div id="app">
  <h1 class="font-black text-white text-2xl"> UPLOAD FILE </h1>
    <h1>Here you can upload your repository and we'll identify and fix vulnerabilities in your open source.</h1> <br>
    <upload-file msg="" />
  </div><br>
  <h2 class="font-black">IT CYBERSECURITY TRENDS 2021</h2> <br>
  <div class="inline-block align-middle">
    <section><iframe width="900" height="506" src="https://www.youtube.com/embed/BP53jX7jAl0" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
    </section>
  </div>

  <div id="app"></div>
</template>

<script>
// @ is an alias to /src
import UploadFile from "@/components/UploadFile.vue";

export default {
  name: "upload",
  components: {
    UploadFile,
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

  color: rgb(241, 233, 233);

  a {
    font-weight: bold;
    color: #8465d1e3;

    &.router-link-exact-active {
      color: #f5f8f7;
    }
  }
}
</style>
