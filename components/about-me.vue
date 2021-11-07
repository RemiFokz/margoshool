<template>
  <div class="about-wrapper">
    <div class="content">
      <h2>Преподаватель</h2>
      <p>
        Внезапно, предприниматели в сети интернет лишь добавляют фракционных
        разногласий и представлены в исключительно положительном свете. Но
        акционеры крупнейших компаний, вне зависимости от их уровня, должны быть
        разоблачены. Идейные соображения высшего порядка, а также выбранный нами
        инновационный путь требует определения и уточнения дальнейших
        направлений развития. Как принято считать, активно развивающиеся страны
        третьего мира и по сей день остаются уделом либералов, которые жаждут
        быть
      </p>
    </div>
    <img class="me" src="/me.png" alt="Марго" />
  </div>
</template>

<script>
export default {}
</script>

<style lang="scss" scoped>
.about-wrapper {
  @include bm;
  border-radius: $brad;
  background: $primary;
  color: white;
  padding: rem(32px);
  @include halfgrid;
  @include font-body(4);
  .me {
    width: 100%;
  }
}
</style>
