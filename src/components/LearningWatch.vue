<template>
  <div class="card text-left">
    <div class="card-body">
      <h4 class="card-title">Watch</h4>

      <p>Count: {{ count }}</p>
      <button class="btn-primary" @click="handleIncrease">Increase</button>
    </div>
  </div>
</template>
<script>
import { ref, watch } from 'vue';

export default {
  setup() {
    const count = ref(0);

    watch(count, (newValue, oldValue) => {
      console.log(newValue, oldValue);
      if (newValue > 10) {
        count.value = 1;
      }
    })

    function handleIncrease() {
      ++count.value;
    }

    return {
      count,
      handleIncrease
    }
  }
}
</script>
<style></style>