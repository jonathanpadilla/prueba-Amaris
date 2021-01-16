<template>
  <div id="app">
    <!--<img alt="Vue logo" src="./assets/logo.png">-->
    <b-container>
      <Autorization />
      <Help />
    </b-container>
  </div>
</template>

<script>
import Autorization from './components/Autorization.vue'
import Help from './components/Help.vue'

export default {
  name: 'App',
  components: {
    Autorization,
    Help
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
