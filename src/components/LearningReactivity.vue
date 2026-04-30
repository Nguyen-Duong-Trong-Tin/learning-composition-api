<template>
  <div class="card text-left">
    <div class="card-body">
      <h4 class="card-title">Learning reactivity</h4>
      <p class="card-text">{{ user.fullName }}</p>
      <p class="card-text">{{ user.age }}</p>
    </div>
  </div>
</template>

<script>
import { reactive, ref } from 'vue';

export default {
  // data() {
  //   return {
  //     fullName: "Nguyen Duong Trong Tin"
  //   }
  // },
  // created() {
  //   setTimeout(() => {
  //     this.fullName = "Nguyen Huynh My Han"
  //   }, 2000)
  // }
  setup() {
    const fullName = ref("Nguyen Duong Trong Tin");
    const age = ref(20);
    const user = reactive({
      fullName: "Nguyen Duong Trong Tin",
      age: 20
    });

    setTimeout(() => {
      fullName.value = "Nguyen Huynh My Han";
      age.value = 18;
      user.fullName = "Nguyen Huynh My Han";
      user.age = 18;
    }, 2000);

    return {
      fullName,
      age,
      user
    }
  }
}
</script>

<style></style>