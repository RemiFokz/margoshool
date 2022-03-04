<template>
  <div class="soon-wrapper">
    <h2>Ближайшие курсы</h2>
    <div class="content">
      <img src="/time.svg" alt="Скоро" />
      <div class="right">
        <CourceCard />
      </div>
    </div>
  </div>
</template>

<script>
export default {}
</script>

<style lang="scss" scoped>
.soon-wrapper {
  @include bm;
  .content {
    @include thirdgrid;
    .right {
      justify-items: end;
      display: grid;
      width: 100%;
    }
  }
}
</style>
