<template>
  <div>
    <img :src="imageUrl" class="img-fluid ${3|rounded-top,rounded-right,rounded-bottom,rounded-left,rounded-circle,|}">
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