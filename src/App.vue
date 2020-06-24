<template>
  <div id="app">
    <!-- <img alt="Vue logo" src="./assets/logo.png">
    <HelloWorld msg="Pomodoro Timer!"/> -->
    <timer />
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import Timer from './components/timer/Timer.vue'
import Picture from './components/picture/Picture.vue'

export default {
  name: 'App',
  components: {
    HelloWorld,
    Timer,
    Picture
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
