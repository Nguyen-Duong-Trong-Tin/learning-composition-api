<template>
  <div class="card text-left">
    <div class="card-body">
      <h4 class="card-title">Template ref</h4>
      <div class="form-group">
        <label>Full name</label>
        <input type="text" class="form-control" id="fullName" ref="fullName">
        <button class="btn btn-primary mt-3" @click="handleClick">Focus</button>
      </div>
    </div>
  </div>
</template>

<script>
import { useTemplateRef } from 'vue';

export default {
  setup() {
    const fullName = useTemplateRef("fullName");

    function handleClick() {
      fullName.value.focus();
    }

    return {
      handleClick
    };
  }
}
</script>

<style></style>