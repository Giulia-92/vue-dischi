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
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
