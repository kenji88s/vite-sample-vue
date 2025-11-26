<template>
  <div class="container">
    <h1>シンプル SPA（コンポーネント化）</h1>

    <ToggleButton :isVisible="isVisible" @toggle="toggle" />

    <MessageBox v-if="isVisible" message="ボタンが押されました！" />
  </div>
</template>

<script setup>
import { ref } from "vue";
import ToggleButton from "./components/ToggleButton.vue";
import MessageBox from "./components/MessageBox.vue";

const isVisible = ref(false);

const toggle = () => {
  isVisible.value = !isVisible.value;
};
</script>

<style scoped>
.container {
  padding: 20px;
  font-family: Arial, sans-serif;
}
</style>
