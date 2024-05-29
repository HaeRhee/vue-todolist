<script setup>
import HelloWorld from "./components/HelloWorld.vue";
</script>

<script>
export default {
  data() {
    return {
      awesome: true,
      title: "Vite + Vue",
    };
  },
};
</script>

<template>
  <div>
    <a href="https://vitejs.dev" target="_blank">
      <img src="/vite.svg" class="logo" alt="Vite logo" />
    </a>
    <a href="https://vuejs.org/" target="_blank">
      <img src="./assets/vue.svg" class="logo vue" alt="Vue logo" />
    </a>
  </div>

  <button type="button" @click="awesome = !awesome">작은 계산기 토글</button>
  <div v-if="awesome"></div>
  <main v-else><HelloWorld :msg="title" /></main>
</template>

<style scoped>
.logo {
  height: 6em;
  padding: 1.5em;
  will-change: filter;
  transition: filter 300ms;
}
.logo:hover {
  filter: drop-shadow(0 0 2em #646cffaa);
}
.logo.vue:hover {
  filter: drop-shadow(0 0 2em #42b883aa);
}
</style>
