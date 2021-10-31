<template>
  <div class="main-wrapper">
    <div class="left">
      <h1>
        Обучение <br />наращиванию ресниц<br />
        в Санкт-Петербурге
      </h1>
      <ui-button>Записаться</ui-button>
    </div>
    <div class="right">
      <img src="" alt="" />
    </div>
  </div>
</template>

<script>
import uiButton from './ui-button.vue'
export default {
  components: { uiButton },
}
</script>

<style lang="scss" scoped>
.main-wrapper {
  grid-template-columns: 3fr 2fr;
  grid-gap: rem(16px);
  display: grid;
  @include bm;
  .left {
    h1 {
      margin-bottom: rem(72px);
    }
  }
}
</style>