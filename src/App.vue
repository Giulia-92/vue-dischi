<template>
  <div id="app">
    <HeaderContent/>
    <MainContent />
  </div>
  
</template>

<script>

import MainContent from './components/MainContent.vue'
import HeaderContent from './components/HeaderContent.vue'
export default {
  name: 'App',
  components: {
    HeaderContent,
    MainContent,
  }
}
</script>

<style lang="scss">
@import "@/assets/styles/general.scss";
</style>
