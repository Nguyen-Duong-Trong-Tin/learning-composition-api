<template>
  <img alt="Vue logo" src="./assets/logo.png">

  <div class="container">
    <learning-reactivity></learning-reactivity>
  </div>
</template>

<script>
import LearningReactivity from './components/LearningReactivity.vue';

export default {
  name: 'App',
  components: {
    LearningReactivity
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
