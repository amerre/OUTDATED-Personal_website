<template>
  <div class="container">
    <appTextBloc :HeticLink="hetic" :GithubLink="github" :CodepenLink="codepen" :EmailLink="email" />
    <appFooter :GithubLink="github" :CodepenLink="codepen" :LinkedinLink="linkedin" />
  </div>
</template>

<script>
import TextBloc from "./components/TextBloc.vue";
import Footer from "./components/Footer.vue";

export default {
  data() {
    return {
      github: "https://github.com/amerre",
      codepen: "https://codepen.io/adrizu/",
      linkedin: "https://www.linkedin.com/in/adrienmerre/",
      email: "mailto:adr.merre@gmail.com",
      hetic: "https://www.hetic.net/formations/grande-ecole"
    };
  },
  components: {
    appTextBloc: TextBloc,
    appFooter: Footer
  }
};
</script>

<style lang="scss">
@import "./assets/scss/_variables.scss";
.container {
  letter-spacing: 0.09px;
  font-family: "Karla", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  width: 810px;
  border: 2px solid red;
  position: relative;
  margin: 100px auto;
}

@import "./assets/scss/_responsive.scss";
</style>
