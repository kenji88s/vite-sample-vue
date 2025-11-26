<template>
  <div class="wrapper">
    <h1>ボタンクリックで切り替え</h1>
    <button @click="toggleView">
      {{ showA ? 'View B に切り替え' : 'View A に切り替え' }}
    </button>

    <div class="view" v-if="showA">
      <h2>View A</h2>
      <p>こちらは A の画面です。</p>
    </div>

    <div class="view" v-else>
      <h2>View B</h2>
      <p>こちらは B の画面です。</p>
    </div>
  </div>
</template>

<script>
export default {
  name: 'App',
  data() {
    return {
      showA: true
    }
  },
  methods: {
    toggleView() {
      this.showA = !this.showA
    }
  }
}
</script>

<style>
.wrapper {
  font-family: sans-serif;
  padding: 2rem;
}

button {
  margin-bottom: 1rem;
  padding: .5rem 1rem;
  cursor: pointer;
}

.view {
  padding: 1rem;
  border: 1px solid #ccc;
  border-radius: .5rem;
}
</style>
