<script setup lang="ts">
import { RouterLink, RouterView } from 'vue-router'
</script>

<template>
  <layoutHeader />
  <RouterView />
</template>

<style lang="scss">
body {
  margin: 0;
  font-family: $font-primary;
}
</style>