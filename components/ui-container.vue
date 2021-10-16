<template>
  <div class="e-container">
    <slot />
  </div>
</template>
<script>
export default {}
</script>
<style lang="scss" scoped>
.e-container {
  box-sizing: border-box;
  padding: rem(0 20px);
  margin: 0 auto;
  width: 100%;
  max-width: rem(1440px);
}
</style>