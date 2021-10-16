<template>
  <component :is="tag" v-on="$listeners">
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
  },
  computed: {
    classes() {
      return {}
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
</style>