<template>
  <footer>
    <ui-container class="cont">
      <ui-logo />
      <ul class="menu">
        <li class="menu-item all">Все курсы</li>
        <li v-for="{ name } in menu" :key="name" class="menu-item">
          {{ name }}
        </li>
      </ul>
      <div class="socials">socials</div>
      <a :href="`tel:${phone}`" class="phone">{{ phone }}</a>
    </ui-container>
  </footer>
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
footer {
  padding: rem(60px) 0;
  background: $primary;
  color: white;
  .cont {
    display: flex;
    justify-content: space-between;
    .menu {
      @include font-body(4);
      display: grid;
      grid-gap: rem(8px);
      &-item {
        cursor: pointer;
      }
    }
    .phone {
      @include font-h(4);
    }
  }
}
</style>
