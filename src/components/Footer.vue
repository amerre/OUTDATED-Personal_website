<template>
  <div class="wrapper">
    <p>
      © 2018 Adrien Merré -
      <a :href="github" class="wrapper__links fab fa-github-square"></a>
      <a :href="codepen" class="wrapper__links fab fa-codepen"></a>
      <a :href="linkedin" class="wrapper__links fab fa-linkedin"></a>
    </p>
  </div>
</template>

<script>
export default {};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import "../scss/_variables.scss";
.wrapper {
  font-size: 16px;
  color: $third-color;
  text-align: center;
  position: absolute;
  bottom: 0;
  width: 810px;
  margin: auto;
  .wrapper__links {
    font-size: 20px;
    margin: 0px 4px;
  }
}
</style>
