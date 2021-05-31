<template>
  <div id="app">
    <h1 class="font-black text-3xl tex-white font-mono">
      CONSCIENTIA IT CYBERSECURITY
    </h1>
    <br />
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
      <img class="rounded-full" alt="Vue logo" src="../assets/logo2.jpg" />
      <div class="text-white">
        <home-debricked msg="" />
      </div>
    </div>
  </div>
  <h2 class="font-black text-3xl font-mono">WEB APP CYBERSECURITY</h2>
  <br />
  <div class="inline-block align-middle text-left font-mono">
    <p>
      Web application security is the process of protecting websites and online
      services against different security threats that exploit vulnerabilities
      in an application’s code. Common targets for web application attacks are
      content management systems (e.g., WordPress), database administration
      tools (e.g., phpMyAdmin) and SaaS applications. Perpetrators consider web
      applications high-priority targets due to: The inherent complexity of
      their source code, which increases the likelihood of unattended
      vulnerabilities and malicious code manipulation.<br />
      High value rewards, including sensitive private data collected from
      successful source code manipulation. .<br />
      <br />
      Ease of execution, as most attacks can be easily automated and launched
      indiscriminately against thousands, or even tens or hundreds of thousands
      of targets at a time. Organizations failing to secure their web
      applications run the risk of being attacked. Among other consequences,
      this can result in information theft, damaged client relationships,
      revoked licenses and legal proceedings.
    </p>
    <br />
  </div>
  <h2 class="font-black text-3xl font-mono">WEB APP VULNERABILITIES</h2>
  <br />

  <div class="text-justify font-mono">
    Typically the result of a lack of input/output sanitization, which are often
    exploited to either manipulate source code or gain unauthorized access.Such
    vulnerabilities enable the use of different attack vectors,including:<br />
    <br />
    <li>
      SQL Injection: Occurs when a perpetrator uses malicious SQL code to
      manipulate a backend database so it reveals information. Consequences
      include the unauthorized viewing of lists, deletion of tables and
      unauthorized administrative access.
    </li>
    <li>
      Cross-site Scripting (XSS) – XSS is an injection attack targeting users in
      order to access accounts, activate Trojans or modify page content.
    </li>
    <li>
      Stored XSS occurs when malicious code is injected directly into an
      application. Reflected XSStakes place when malicious script is reflected
      off of an application onto a user’s browser.
    </li>
    <li>
      Remote File Inclusion: A hacker uses this type of attack to remotely
      inject a file onto a web application server. This can result in the
      execution of malicious scripts or code within the application, as well as
      data theft or manipulation.
    </li>
    <li>
      Cross-site Request Forgery (CSRF): An attack that could result in an
      unsolicited transfer of funds, changed passwords or data theft. It’s
      caused when a malicious web application makes a user’s browser perform an
      unwanted action in a site to which a user is logged on.
    </li>
    <br />
    <p>
      In theory,thorough input/output sanitization could eliminate all
      vulnerabilities, making an application immune to unlawful manipulation.
      However, complete sanitization usually isn’t a practical option, since
      most applications exist in a constant development state. Moreover,
      applications are also frequently integrated with each other to create an
      increasingly complex coded environment. Web application security solutions
      and enforced security procedures, such as PCI Data Security Standard (PCI
      DSS) certification, should be deployed to avoid such threats.
    </p>
  </div>

  <br />
  
  <br />
  <br />
  <h2 class="font-black text-3xl  font-mono">IMPORTANCE OF IT CYBERSECURITY</h2>
  <br />
  <div class="inline-block align-middle">
    <section>
      <iframe
        width="900"
        height="506"
        src="https://www.youtube.com/embed/ZOtQ21hXJ7k"
        title="YouTube video player"
        frameborder="0"
        allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
        allowfullscreen
      ></iframe>
    </section>
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
