<template>
  <div id="app">
    <MadeWithLove by="Raj Kharvar" link="https://github.com" />
  </div>
</template>

<script>
import MadeWithLove from './components/MadeWithLove.vue'

export default {
  name: 'App',
  components: {
    MadeWithLove
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
}
</style>
