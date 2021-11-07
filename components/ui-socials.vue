<template>
  <div class="soc-wrapper"></div>
</template>

<script>
import { mapState } from 'vuex'
export default {
  computed: {
    ...mapState(['socials']),
  },
}
</script>

<style></style>
