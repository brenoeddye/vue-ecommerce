<script lang="ts">
import { defineComponent } from 'vue'

export default defineComponent({
    data() {
      return {
        dataTheme: document.documentElement.getAttribute('data-theme') || document.documentElement.setAttribute('data-theme', 'dark')
      }
    },
    mounted() {
      document.documentElement.setAttribute('data-theme', localStorage.getItem('data-theme'));
    },
    watch: {
      dataTheme(newTheme) {
        localStorage.setItem('data-theme', newTheme);
        document.documentElement.setAttribute('data-theme', newTheme);
      }
    }
})
</script>

<template>
  <layoutHeader @changeTheme="dataTheme == 'dark' ? dataTheme = 'light' : dataTheme = 'dark' "/>
  <RouterView />
</template>

<style lang="scss">
body {
  margin: 0;
  font-family: $font-primary;
  color: var(--font-color);
  background-color: var(--tertiary-alt);
  transition: all .3s linear;
}
</style>