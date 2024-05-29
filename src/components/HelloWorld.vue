<script setup>
import { ref } from "vue";

defineProps({
  msg: String,
});

const count = ref(0);
const discount = ref(0);
const totalCount = ref(count + discount);
const limitCount = totalCount > 0 ? discount : count;
const countNumber = ref(limitCount);
// console.log(count);
</script>

<template>
  <section class="wrap">
    <h1>{{ msg }}</h1>

    <div class="card">
      {{ count + discount }}
      <button type="button" @click="count++">count is {{ limitCount }}</button>
      <button type="button" @click="discount--">
        discount is {{ discount }}
      </button>
      {{ console.log(count) }}
      {{ console.log(discount) }}
      <p>
        Edit
        <code>components/HelloWorld.vue</code> to test HMR
      </p>
    </div>

    <p>
      Check out
      <a href="https://vuejs.org/guide/quick-start.html#local" target="_blank"
        >create-vue</a
      >, the official Vue + Vite starter
    </p>
    <p>
      Install
      <a href="https://github.com/vuejs/language-tools" target="_blank"
        >Volar</a
      >
      in your IDE for a better DX
    </p>
    <p class="read-the-docs">Click on the Vite and Vue logos to learn more</p>
  </section>
</template>

<style scoped>
.read-the-docs {
  color: #888;
}
</style>
