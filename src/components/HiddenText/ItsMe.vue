<template>
  <span class="hiddenWrapper">
    <p>Yes, it’s definitely me</p>
  </span>
</template>

<script>
export default {};
</script>

<style scoped lang="scss">
@import "../../scss/_variables.scss";
.hiddenWrapper {
  p {
    position: absolute;
    top: -90px;
    left: 40px;
    width: 200px;
    transform: rotate(8deg);
    font-size: 20px;
  }
}
</style>
