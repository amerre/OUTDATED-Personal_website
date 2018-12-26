<template>
  <span class="wrapper">
    <a :href="linkUrl" target="_blank">{{ linkText }}</a>
  </span>
</template>

<script>
export default {
  data() {
    return {
      selectedLink: this.linkText
    };
  },
  props: {
    linkText: String,
    linkUrl: String
  }
};
</script>

<style scoped lang="scss">
@import "../assets/scss/_variables.scss";
a {
  text-decoration: none;
  color: $first-color;
  background-position-y: 0;
  background: linear-gradient(180deg, $second-color, $second-color) no-repeat 0
    1.2rem;
  transition: background-position-y 0.15s ease-out;
  &:hover {
    background-position-y: 0;
  }
}
@import "../assets/scss/_responsive.scss";
</style>
