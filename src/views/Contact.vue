<template>
  <div id="app">
    <contact-debricked msg="" />
    <!-- Right area -->
    <div class="w-2/6 p-5 inline-block align-middle">
      <div class="justify-center h-full rounded-sm text-white">
        <div class="">
          <img
            class="rounded-full"
            src="../assets/security.jpg"
            alt="Security"
          />

          <div class="2xl:text-lg text-yellow">
            <p></p>
          </div>
          <br />
          <div class="2xl:py-2 2xl:text-lg text-white-400">
            Alexander Garcia Angus <br />

            <svg
              class="w-5 right h-5 inline-block align-middle mr-3 2xl:w-5 2xl:h-5"
              fill="none"
              stroke="currentColor"
              viewBox="0 0 24 24"
              xmlns="http://www.w3.org/2000/svg"
            >
              <path
                stroke-linecap="round"
                stroke-linejoin="round"
                stroke-width="2"
                d="M3 8l7.89 5.26a2 2 0 002.22 0L21 8M5 19h14a2 2 0 002-2V7a2 2 0 00-2-2H5a2 2 0 00-2 2v10a2 2 0 002 2z"
              />
            </svg>
            <p>
              <a
                target="_blank"
                href="mailto:conscientia.digitaltech@gmail.com"
              >
                conscientia.digitaltech@gmail.com</a
              >
            </p>
            Malmö, Sweden
          </div>
        </div>
      </div>
    </div>
  </div>

  <div id="app"></div>
</template>

<script>
// @ is an alias to /src

import ContactDebricked from "../components/ContactDebricked.vue";

export default {
  name: "Contact",
  components: {
    ContactDebricked,
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
