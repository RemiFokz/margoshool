<template>
  <div class="soon-wrapper">
    <h2>Ближайшие курсы</h2>
    <div class="content">
      <img src="" alt="" />
      <div class="right">
        <CourceCard />
      </div>
    </div>
  </div>
</template>

<script>
export default {}
</script>

<style lang='scss' scoped>
.soon-wrapper {
  @include bm;
  .content {
    @include halfgrid;
  }
}
</style>