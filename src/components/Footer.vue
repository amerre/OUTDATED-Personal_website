<template>
  <div class="footer">
    <p>
      © 2018 Adrien Merré -
      <a
        :href="github"
        class="footer__links fab fa-github-square"
        target="_blank"
      ></a>
      <a :href="codepen" class="footer__links fab fa-codepen" target="_blank"></a>
      <a :href="linkedin" class="footer__links fab fa-linkedin" target="_blank"></a>
    </p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      github: "https://github.com/amerre",
      codepen: "https://codepen.io/adrizu/",
      linkedin: "https://www.linkedin.com/in/adrienmerre/"
    };
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import "../scss/_variables.scss";
.footer {
  font-size: 16px;
  color: $third-color;
  text-align: center;
  width: 810px;
  margin: auto;
  height: 50px;
  box-sizing: border-box;
  .footer__links {
    font-size: 20px;
    text-decoration: none;
    color: $third-color;
    margin: 0px 4px;
    &:hover {
      color: $second-color;
    }
  }
}
</style>
