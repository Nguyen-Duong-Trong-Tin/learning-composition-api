<template>
  <div class="card text-left">
    <div class="card-body">
      <h4 class="card-title">Lifecycle hook</h4>
    </div>
  </div>
</template>
<script>
import { onBeforeMount, onMounted } from 'vue';

export default {
  setup() {
    console.log("Before created");
    console.log("Created");

    onBeforeMount(() => {
      console.log("Before mount");
    });
    onMounted(() => {
      console.log("Mounted");
    });
  }
}
</script>
<style></style>