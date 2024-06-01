<script setup>
import HelloWorld from "./components/HelloWorld.vue";
import ListRendering from "./components/ListRendering.vue";
</script>

<script>
export default {
  data() {
    return {
      openCalculator: true,
      title: { HelloWorld: "Vite + Vue", ListRendering: "Vue Study" },
      items: [{ message: "뷰 공부하기" }, { message: "투두리스트 만들기" }],
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
  <ListRendering />
  <br />
  <button type="button" @click="openCalculator = !openCalculator">
    작은 계산기 토글
  </button>
  <div v-if="openCalculator"></div>
  <main v-else>
    <HelloWorld :msg="title.HelloWorld" />
  </main>
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
