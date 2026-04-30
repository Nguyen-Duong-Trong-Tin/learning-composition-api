<template>
  <div class="card text-left">
    <div class="card-body">
      <h4 class="card-title">Computed</h4>

      <div class="form-group">
        <label>First name</label>
        <input type="text" class="form-control" @input="handleChangeFirstName">
      </div>
      <div class="form-group">
        <label>Last name</label>
        <input type="text" class="form-control" @input="handleChangeLastName">
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

    function handleChangeFirstName(event) {
      firstName.value = event.target.value;
    }
    function handleChangeLastName(event) {
      lastName.value = event.target.value;
    }

    const fullName = computed(() => `${firstName.value} ${lastName.value}`);

    return {
      handleChangeFirstName,
      handleChangeLastName,
      fullName
    }
  }
}
</script>
<style></style>