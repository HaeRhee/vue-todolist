<script setup>
const title = "Vue Study";
const items = [
  { id: 1, content: "뷰 공부하기" },
  { id: 2, content: "투두리스트 만들기" },
];
</script>
<template>
  <main>
    <h1>
      {{ title }}
    </h1>
    <ul v-for="item in items" :key="item.id">
      <li>
        {{ item.id + ". " + item.content }}
      </li>
    </ul>
  </main>
</template>

<style></style>
