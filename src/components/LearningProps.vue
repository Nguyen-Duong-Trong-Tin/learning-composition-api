<template>
  <div class="card text-left">
    <div class="card-body">
      <h4 class="card-title">Props</h4>
      <img class="card-img-top" :src="imageUrl">
    </div>
  </div>
</template>
<script>
import { toRefs } from 'vue';

export default {
  props: {
    imageUrl: {
      type: String
    }
  },
  setup(props) {
    const { imageUrl } = toRefs(props)
    console.log(imageUrl);
  }
}
</script>
<style></style>