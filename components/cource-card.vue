<template>
  <div class="card-wrapper">
    <h4>{{ title }}</h4>
    <ul class="body-text">
      <li v-for="({ key, value }, i) in items" :key="i">
        <div>{{ key }}</div>
        <div>{{ value }}</div>
      </li>
    </ul>
    <div class="btns">
      <ui-button secondary>Подробнее</ui-button>
      <ui-button>Записаться</ui-button>
    </div>
  </div>
</template>

<script>
import uiButton from './ui-button.vue'
export default {
  components: { uiButton },
  props: {
    items: {
      type: Array,
      default: () => [],
    },
    title: {
      type: String,
      default: 'Курс',
    },
  },
}
</script>

<style lang="scss" scoped>
.card-wrapper {
  min-height: rem(480px);
  padding: rem(24px);
  max-width: rem(400px);
  border-radius: $brad;
  display: grid;
  width: 100%;
  grid-template-rows: max-content 1fr max-content;
  background: $secondary;
  color: white;
  h4 {
    margin-bottom: rem(48px);
  }
  .btns {
    display: grid;
    grid-gap: rem(8px);
  }
}
</style>
