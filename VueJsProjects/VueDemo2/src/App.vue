<template>
  <div id="app">
    <!--<img alt="Vue logo" src="./assets/logo.png">
    <HelloWorld msg="Welcome to Your Vue.js App"/>-->
    <StarWarsPeople></StarWarsPeople>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import StarWarsPeople from "./components/StarWarsPeople";

export default {
  name: 'app',
  components: {
    HelloWorld,
    StarWarsPeople
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
