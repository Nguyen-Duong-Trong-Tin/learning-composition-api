<template>
  <div class="card text-left">
    <div class="card-body">
      <h4 class="card-title">Computed</h4>

      <div class="form-group">
        <label>First name</label>
        <input type="text" class="form-control" v-model="firstName">
      </div>
      <div class="form-group">
        <label>Last name</label>
        <input type="text" class="form-control" v-model="lastName">
      </div>

      <p class="card-text">Fullname: {{ fullName }}</p>

    </div>
  </div>
</template>
<script>
import { computed, ref } from 'vue';

export default {
  setup() {
    const firstName = ref("");
    const lastName = ref("");

    const fullName = computed(() => `${firstName.value} ${lastName.value}`);

    return {
      firstName,
      lastName,
      fullName
    }
  }
}
</script>
<style></style>