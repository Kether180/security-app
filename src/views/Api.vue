<template>
  <div id="app">
    <api-interface msg="" />
    <h1 class="text-white text-4xl  font-black">
      Repositories
    </h1>
    <br />
    <h1 class="text-white text-2xl text-left  font-black">
      Repositories
    </h1>
    <br />
    <div class="place-self-strech">
      <table class="border-collapse  border-green-800">
        <thead>
          <tr>
            <th class="text-white border border-green-600">ID</th>
            <th class="text-white border border-green-600">File Name</th>
            <th class="text-white border border-green-600">Branch Name</th>
            <th class="text-white border border-green-600">Product Name</th>
            <th class="text-white border border-green-600">>Release Name</th>
            <th class="text-white border border-green-600">Repository URL</th>
            <th class="text-white border border-green-600">Branch Name</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <td class="text-white border border-green-600">1</td>
            <td class="text-white border border-green-600"></td>
            <td class="text-white border border-green-600"></td>
            <td class="text-white border border-green-600"></td>
            <td class="text-white border border-green-600"></td>
            <td class="text-white border border-green-600"></td>
            <td class="text-white border border-green-600"></td>
          </tr>
          <tr>
            <td class="text-white border border-green-600">2</td>
            <td class="text-white border border-green-600"></td>
            <td class="text-white border border-green-600"></td>
            <td class="text-white border border-green-600"></td>
            <td class="text-white border border-green-600"></td>
            <td class="text-white border border-green-600"></td>
            <td class="text-white border border-green-600"></td>
          </tr>
          <tr>
            <td class="text-white border border-green-600">3</td>
            <td class="text-white border border-green-600"></td>
            <td class="text-white border border-green-600"></td>
            <td class="text-white border border-green-600"></td>
            <td class="text-white border border-green-600"></td>
            <td class="text-white border border-green-600"></td>
            <td class="text-white border border-green-600"></td>
          </tr>
        </tbody>
      </table>
    </div>

    <h2 class="text-white text-align: text-2xl text-left  font-black">
      <br />
      Vulnerabilities
    </h2>
    <h3 class="text-whitetext-align: text-2xl text-left  font-black">
      <br />
      Dependencies
    </h3>
    <h4 class="text-white text-align: text-2xl text-left font-black">
      <br />
      Licenses
    </h4>
  </div>

  <div id="app"></div>
</template>

<script>
// @ is an alias to /src

import ApiInterface from "../components/ApiInterface.vue";

export default {
  name: "Api",
  components: {
    ApiInterface,
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
