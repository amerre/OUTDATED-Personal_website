<template>
  <div class="container">
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

.container {
  letter-spacing: 0.09px;
  font-family: "Karla", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  width: 810px;
  position: relative;
  margin: 150px auto auto auto;
}
@media (max-width: 1008px) {
  .container {
    width: calc(100% - 150px);
    margin-top: 100px;
  }
  .footer {
    width: 100% !important;
  }
  .wrapper {
    min-height: calc(100vh - 170px) !important;
  }
}
@media (max-width: 640px) {
  .container {
    width: calc(100% - 30px);
    margin-top: 50px;
  }
  .footer {
    width: 100% !important;
    font-size: 14px !important;
    .footer__links {
      font-size: 18px !important;
    }
  }
  .wrapper {
    min-height: calc(100vh - 120px) !important;
    p {
      font-size: 18px !important;
    }
  }
  .hiddenWrapper {
    display: none;
  }
}
</style>
