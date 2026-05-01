<template>
  <div class="card text-left">
    <div class="card-body">
      <h4 class="card-title">Provide/inject</h4>

      <p>App name: {{ appName }}</p>
      <p>App age: {{ appAge }}</p>
    </div>
  </div>
</template>

<script>
import { inject } from 'vue';

export default {
  setup() {
    const appName = inject("appName", "Default app name");
    const appAge = inject("appAge");

    return {
      appName,
      appAge
    }
  }
}
</script>

<style></style>