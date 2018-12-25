<template>
  <div id="app">
    <TextBloc/>
    <Footer/>
  </div>
</template>

<script>
import TextBloc from "./components/TextBloc.vue";
import Footer from "./components/Footer.vue";

export default {
  name: "app",
  data() {
    return {
      github: "https://github.com/amerre",
      codepen: "https://codepen.io/adrizu/",
      hetic: "https://www.hetic.net/formations/grande-ecole"
    };
  },
  components: {
    TextBloc,
    Footer
  }
};
</script>

<style lang="scss">
@import "./scss/_variables.scss";
#app {
  letter-spacing: 0.09px;
  font-family: "Karla", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  width: 810px;
  margin: 150px auto auto auto;
}
</style>
