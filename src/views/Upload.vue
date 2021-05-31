<template>
  <div id="app">
   
    <h1 class="font-black text-3xl font-mono">
    WEB APP SECURITY CHECKLIST "OUR SERVICES"
  </h1>

  <br />

  <div class="text-white text-justify font-mono">
    There are a number of methods for securing web applications. The following
    processes should be part of any web application security checklist:<br />
    <br />
    <li>
      Information gathering – Manually review the application, identifying entry
      points and client-side codes. Classify third-party hosted content.
    </li>

    <li>
      Authorization – Test the application for path traversals; vertical and
      horizontal access control issues; missing authorization and insecure,
      direct object references.
    </li>
    <li>
      Cryptography – Secure all data transmissions. Has specific data been
      encrypted? Have weak algorithms been used? Do randomness errors exist?
      Denial of service
    </li>
    <li>
      Improve an application’s resilience against denial of service threats by
      testing for anti-automation, account lockout, HTTP protocol DoS and SQL
      wildcard DoS. This doesn’t cover protection from high-volume DoS and DDoS
      attacks, which are best countered by a combination of filtering solutions
      and scalable resources.
    </li>
  </div>
    

    <br />
    <h1 class="font-black text-white text-3xl font-mono">
      UPLOAD FILE : Here you can upload your repository and we'll identify and
      fix vulnerabilities in your open source.
    </h1>

    <br />
    <upload-file msg="" />
  </div>
  <br />

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
