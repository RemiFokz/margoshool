<template>
  <div class="all-wrapper">
    <h2>Все курсы</h2>
    <div class="content">
      <CourceCard />
      <div class="info">
        <ul class="list">
          <li v-for="(name, i) in courses" :key="name" @click="active = i">
            <ui-button woh :secondary="active !== i">{{ name }}</ui-button>
          </li>
        </ul>
        <img src="" alt="" />
      </div>
    </div>
  </div>
</template>

<script>
import uiButton from './ui-button.vue'
export default {
  components: { uiButton },
  data() {
    return {
      active: 0,
      courses: [
        'Базовый курс',
        '2-3D объем',
        'Обьем 4D и более',
        'Трендовые эффекты',
      ],
    }
  },
}
</script>

<style lang="scss" scoped>
.all-wrapper {
  @include bm;
  .content {
    @include twogrid;
    ul {
      display: flex;
      flex-wrap: wrap;
      align-items: flex-start;
      li {
        margin-right: rem(16px);
        margin-bottom: rem(16px);
      }
    }
  }
}
</style>
