<template>
  <div class="wrapper">
    <appTextBloc/>
    <appFooter/>
  </div>
</template>

<script>
import TextBloc from "./components/TextBloc.vue";
import Footer from "./components/Footer.vue";

export default {
  name: "app",
  components: {
    appTextBloc: TextBloc,
    appFooter: Footer
  }
};
</script>

<style lang="scss">
@import "./scss/_variables.scss";

.wrapper {
  letter-spacing: 0.09px;
  font-family: "Karla", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  width: 810px;
  position: relative;
  margin: 100px auto auto auto;
}
</style>
