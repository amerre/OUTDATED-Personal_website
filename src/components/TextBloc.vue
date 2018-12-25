<template>
  <div class="wrapper">
    <span class="wrapper__emoji">👨🏻‍💻</span>
    <p>Hi, I’m Adrien</p>
    <p>I’m living in Montreuil, near Paris, where I’m studying in
      <app-Link linkText="hetic"/>. I’m playing around with web development, design and project management.
    </p>
    <p>I’m actualy a front-end developer, but currently learning Vue.js and Node.js in order to become a full-stack Javascript ninja.</p>
    <p>To see some of my work, check my
      <app-Link linkText="Github"/>&nbsp;or my
      <app-Link linkText="Codepen"/>.
    </p>
    <p>
      I’m open to any work propositions, but I’m looking especially for an 5-month internship in June 2019, feel free to drop me a line at
      <a
        class="wrapper__bold"
      >adr.merre@gmail.com</a>.
    </p>
    <div class="wrapper__hidden">
      <h1>Hello</h1>
    </div>
  </div>
</template>

<script>
import Link from "../components/Link.vue";
export default {
  components: {
    appLink: Link
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import "../scss/_variables.scss";
.wrapper {
  line-height: 27px;
  .wrapper__emoji {
    font-size: 55px;
  }
  p {
    font-size: 20px;
    color: $first-color;
  }
  .wrapper__underline {
    background-color: $second-color;
    text-decoration: none;
    color: $first-color;
  }
  .wrapper__bold {
    font-weight: bold;
    color: $second-color;
  }
  .wrapper__hidden {
    display: none;
  }
}
</style>
