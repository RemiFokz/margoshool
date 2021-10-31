<template>
  <component :is="tag" :class="classes" class="btn" v-on="$listeners">
    <slot />
  </component>
</template>

<script>
export default {
  props: {
    to: {
      type: String,
      default: '',
    },
    href: {
      type: String,
      default: '',
    },
    secondary: {
      type: Boolean,
      default: false,
    },
  },
  computed: {
    classes() {
      return {
        secondary: this.secondary,
      }
    },
    tag() {
      if (this.to) {
        return 'nuxt-link'
      }
      if (this.href) {
        return 'a'
      }
      return 'button'
    },
  },
}
</script>


<style lang="scss" scoped>
.btn {
  background: $primary;
  padding: rem(16px);
  border: 1px solid $primary;
  font-weight: 500;
  color: white;
  border-radius: $brad;
  transition: color 0.3s ease-out, background 0.25s ease-in;
  &:hover {
    color: $primary;
    background: transparent;
    border: 1px solid $primary;
  }
  &.secondary {
    color: $primary;
    background: transparent;
    border: 1px solid $primary;
    &:hover {
      color: white;
      background: $primary;
      border: 1px solid $primary;
    }
  }
}
</style>