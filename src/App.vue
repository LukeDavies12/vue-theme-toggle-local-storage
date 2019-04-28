<template>
  <div id="app">
    <Navbar/>
    <router-view/>
  </div>
</template>

<script>
import Navbar from '@/components/Navbar.vue'
export default {
  components: {
    Navbar
  }
}
</script>


<style lang="scss">
@import './assets/scss/theme.scss';
@import './assets/scss/base.scss'
</style>
