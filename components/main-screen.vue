<template>
  <div class="main-wrapper">
    <div class="left">
      <h1>
        Обучение <br />наращиванию ресниц<br />
        в <span>Санкт-Петербурге</span>
      </h1>

      <ui-button>Записаться</ui-button>
    </div>
    <div class="right">
      <img src="/main.svg" alt="Обучение" />
    </div>
  </div>
</template>

<script>
export default {}
</script>

<style lang="scss" scoped>
.main-wrapper {
  grid-template-columns: 1fr 1fr;
  grid-gap: rem(16px);
  display: grid;
  @include bm;
  min-height: rem(600px);
  align-items: center;
  .left {
    h1 {
      margin-bottom: rem(72px);
      span {
        color: $primary;
      }
    }
  }
  .right {
    width: 100%;
    img {
      width: 100%;
      height: 100%;
    }
  }
}
</style>
