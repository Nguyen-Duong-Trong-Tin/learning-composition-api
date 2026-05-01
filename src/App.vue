<template>
  <img alt="Vue logo" src="./assets/logo.png">

  <div class="container">
    <learning-reactivity></learning-reactivity>
    <div class="mb-3"></div>

    <learning-prop imageUrl="https://images.pexels.com/photos/19884401/pexels-photo-19884401.jpeg"></learning-prop>
    <div class="mb-3"></div>

    <learning-method></learning-method>
    <div class="mb-3"></div>

    <learning-computed></learning-computed>
    <div class="mb-3"></div>

    <learning-watch></learning-watch>
    <div class="mb-3"></div>

    <learning-template-ref></learning-template-ref>
    <div class="mb-3"></div>

    <learning-provide-inject></learning-provide-inject>
  </div>
</template>

<script>
import LearningReactivity from './components/LearningReactivity.vue';
import LearningProp from './components/LearningProps.vue';
import LearningMethod from './components/LearningMethod.vue';
import LearningComputed from './components/LearningComputed.vue';
import LearningWatch from './components/LearningWatch.vue';
import LearningTemplateRef from './components/LearningTemplateRef.vue';
import LearningProvideInject from './components/LearningProvideInject.vue';
import { provide, ref } from 'vue';

export default {
  name: 'App',
  components: {
    LearningReactivity,
    LearningProp,
    LearningMethod,
    LearningComputed,
    LearningWatch,
    LearningTemplateRef,
    LearningProvideInject
  },
  setup() {
    const appAge = ref(1);

    provide("appName", "Learning composition API");
    provide("appAge", appAge);

    setInterval(() => {
      ++appAge.value;
    }, 2000);
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
