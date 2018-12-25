<template>
  <a href="http://google.fr">{{ linkText }}</a>
</template>

<script>
export default {
  props: ["linkText"]
};
</script>

<style scoped lang="scss">
@import "../scss/_variables.scss";
a {
  text-decoration: none;
  color: $first-color;
  background-position-y: 0;
  display: inline;
  background: linear-gradient(180deg, $second-color, $second-color) no-repeat 0
    1.2rem;
  transition: background-position-y 0.15s ease-out;
}
a:hover {
  background-position-y: 0;
}
</style>