<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <div id="app">
    <MyConversor coin-a="USD" coin-b="BRL"/>
  </div>
</template>

<script>
import MyConversor from "./components/MyConversor.vue"

export default {
  name: 'App',
  components: {
    MyConversor
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
