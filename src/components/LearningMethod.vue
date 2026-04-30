<template>
  <div class="card text-left">
    <div class="card-body">
      <h4 class="card-title">Methods</h4>
      <p class="card-text">{{ user.fullName }}</p>
      <p class="card-text">{{ user.age }}</p>
      <button class="btn btn-primary" @click="handleChangeUser">Change</button>
    </div>
  </div>
</template>

<script>
import { reactive } from 'vue';

export default {
  setup() {
    const user = reactive({
      fullName: "Nguyen Duong Trong Tin",
      age: 20
    });

    function handleChangeUser() {
      user.fullName = "Nguyen Huynh My Han";
      user.age = 18;
    }

    return {
      user,
      handleChangeUser
    }
  }
}
</script>

<style></style>