<template>
  <img alt="Vue logo" src="./assets/logo.png">

  <div class="container">
    <learning-reactivity></learning-reactivity>

    <div class="my-3"></div>

    <learning-prop imageUrl="https://images.pexels.com/photos/19884401/pexels-photo-19884401.jpeg"></learning-prop>

    <learning-method></learning-method>
  </div>
</template>

<script>
import LearningReactivity from './components/LearningReactivity.vue';
import LearningProp from './components/LearningProps.vue';
import LearningMethod from './components/LearningMethod.vue';

export default {
  name: 'App',
  components: {
    LearningReactivity,
    LearningProp,
    LearningMethod
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
