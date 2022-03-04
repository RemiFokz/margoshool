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
    small: {
      type: Boolean,
      default: false,
    },
    big: {
      type: Boolean,
      default: false,
    },
    woh: {
      type: Boolean,
      default: false,
    },
  },
  computed: {
    classes() {
      return {
        secondary: this.secondary,
        small: this.small,
        big: this.big,
        woh: this.woh,
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
  padding: rem(16px 24px);
  border: 1px solid $primary;

  color: white;
  border-radius: $brad;
  transition: color 0.3s ease-out, background 0.25s ease-in;
  @include font-body(1);
  text-transform: capitalize;
  font-weight: 500;
  &:hover:not(.woh) {
    color: $primary;
    background: transparent;
    border: 1px solid $primary;
  }

  &.secondary {
    color: $primary;
    background: transparent;
    border: 1px solid $primary;
    &:hover:not(.woh) {
      color: white;
      background: $primary;
      border: 1px solid $primary;
    }
  }
  &.small {
    padding: rem(8px) rem(16px);
    @include font-body(2);
    border-radius: $bradsmall;
    font-weight: 500;
  }
  &.big {
    padding: rem(16px) rem(32px);
    @include font-body(4);
    font-weight: 500;
  }
}
</style>
