<template>
  <nav>
    <ui-container class="menu-wrapper">
      <ui-logo />
      <ul class="menu">
        <li class="menu-item all">Все курсы +</li>
        <li v-for="{ name } in menu" :key="name" class="menu-item">
          {{ name }}
        </li>
      </ul>
      <a :href="`tel:${phone}`" class="phone">{{ phone }}</a>
      <ui-button small>Записаться</ui-button>
    </ui-container>
  </nav>
</template>

<script>
import { mapState } from 'vuex'

export default {
  computed: {
    ...mapState(['menu', 'courses', 'phone']),
  },
}
</script>

<style lang="scss" scoped>
nav {
  position: fixed;
  left: 0;
  right: 0;
  background: white;
  .menu-wrapper {
    display: grid;
    grid-template-columns: max-content 1fr max-content max-content;
    grid-gap: rem(16px);
    height: rem(60px);
    align-items: center;
    justify-content: space-between;
    @include font-body(4);
    font-weight: 500;
    .menu {
      justify-self: end;
      display: flex;
      .all {
        margin-right: rem(16px);
        cursor: pointer;
        position: relative;
      }
      &-item:not(.all) {
        margin-right: rem(16px);
        cursor: pointer;
        position: relative;
        &:after {
          content: '';
          height: 2px;
          width: 100%;
          position: absolute;
          background: $primary;
          bottom: -4px;
          left: 0;
          transform: scale(0);
          transition: transform 0.2s ease-in;
        }
        &:hover {
          &:after {
            transform: scale(1);
          }
        }
      }
    }
  }
}
</style>
