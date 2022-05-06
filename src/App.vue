<template>
  <div id="app">
    <MainContent />
  </div>
  
</template>

<script>

import MainContent from './components/MainContent.vue'

export default {
  name: 'App',
  components: {
    
    MainContent
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
