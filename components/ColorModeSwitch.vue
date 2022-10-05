<template>
  <CIconButton
    mr="3"
    :icon="colorMode === 'light' ? 'moon' : 'sun'"
    :aria-label="`Switch to ${colorMode === 'light' ? 'dark' : 'light'} mode`"
    @click="toggleColorMode"
  />
</template>

<script>
export default {
  inject: ['$chakraColorMode', '$toggleColorMode'],

  data() {
    return {}
  },
  computed: {
    colorMode() {
      return this.$chakraColorMode()
    },
    theme() {
      return this.$chakraTheme()
    },
    toggleColorMode() {
      return this.$toggleColorMode
    },
  },
}
</script>

<style></style>
