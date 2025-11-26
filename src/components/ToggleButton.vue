<template>
  <button @click="$emit('toggle')">
    {{ isVisible ? "非表示にする" : "表示する" }}
  </button>
</template>

<script setup>
defineProps({
  isVisible: Boolean
});
</script>

<style scoped>
button {
  padding: 10px 20px;
  cursor: pointer;
}
</style>
