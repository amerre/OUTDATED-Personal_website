<template>
  <span class="hiddenWrapper">
    <p>Oui, c'est vraiment moi</p>
  </span>
</template>

<script>
export default {};
</script>

<style scoped lang="scss">
@import "../../assets/scss/_variables.scss";
.hiddenWrapper {
  p {
    position: absolute;
    top: -60px;
    left: 40px;
    width: 250px;
    transform: rotate(8deg);
    font-size: 20px;
  }
}
</style>
