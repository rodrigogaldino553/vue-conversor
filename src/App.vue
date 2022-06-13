<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <h1>Coin Conversor</h1>
  <div id="app">
    <div class="line">
      <MyConversor coin-a="USD" coin-b="BRL"/>
      <MyConversor coin-a="BRL" coin-b="USD"/>
    </div>
    <div class="line">
      <MyConversor coin-a="CAD" coin-b="BRL"/>
      <MyConversor coin-a="BRL" coin-b="CAD"/>
    </div>
    <div class="line">
      <MyConversor coin-a="EUR" coin-b="BRL"/>
      <MyConversor coin-a="BRL" coin-b="EUR"/>
    </div>
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
  max-width: 900px;
  margin: auto;
}

.line{
  display: flex;
  justify-content: space-around;
  margin-top: 40px;
}
</style>
