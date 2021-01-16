<template>
  <div id="app">
    <!--<img alt="Vue logo" src="./assets/logo.png">-->
    <b-container>
      <Autorization msg="Hola" />
    </b-container>
  </div>
</template>

<script>
import Autorization from './components/Autorization.vue'

export default {
  name: 'App',
  components: {
    Autorization
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
