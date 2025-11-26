<template>
  <div class="box">
    {{ message }}
  </div>
</template>

<script setup>
defineProps({
  message: String
});
</script>

<style scoped>
.box {
  margin-top: 20px;
  padding: 15px;
  border: 1px solid #999;
  background: #f9f9f9;
}
</style>
