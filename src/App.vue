<template>
  <div id="app">
    <DischiContent/>
  </div>
  
</template>

<script>
import DischiContent from './components/DischiContent.vue'

export default {
  name: 'App',
  components: {
    DischiContent
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
