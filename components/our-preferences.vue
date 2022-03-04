<template>
  <div class="our-wrapper">
    <h2>Наши преимущества</h2>
    <div class="content">
      <img src="/we.svg" alt="Наши преимущества" />
      <ul class="list">
        <li v-for="name in adv" :key="name">{{ name }}</li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      adv: [
        'Делаем упор на практику',
        'Учимся общению с клиентом на реальных кейсах',
        'Внедряем лайфхаки в рабочий процесс',
        'Общаемся в чате, в том числе после окончания обучения',
        'Получаем необычную и супер информативную методичку',
      ],
    }
  },
}
</script>

<style lang="scss" scoped>
.our-wrapper {
  @include bm;
  .content {
    @include thirdgrid;
    align-items: start;
    img {
      width: 100%;
    }
    ul {
      display: grid;
      grid-gap: rem(16px);
      @include font-body(4);
      font-weight: 500;
      margin-top: rem(100px);
    }
  }
}
</style>
