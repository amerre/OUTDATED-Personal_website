<template>
  <div class="footer">
    <p>
      © 2018 Adrien Merré -
      <a
        :href="GithubLink"
        class="footer__links fab fa-github-square"
        target="_blank"
      ></a>
      <a :href="CodepenLink" class="footer__links fab fa-codepen" target="_blank"></a>
      <a :href="LinkedinLink" class="footer__links fab fa-linkedin" target="_blank"></a>
    </p>
  </div>
</template>

<script>
export default {
  props: {
    GithubLink: String,
    CodepenLink: String,
    LinkedinLink: String
  }
};
</script>

<style scoped lang="scss">
@import "../assets/scss/_variables.scss";
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
@import "../assets/scss/_responsive.scss";
</style>
