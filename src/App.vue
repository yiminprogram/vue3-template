<template>
  <h1 class="text-5xl font-bold p-3">{{ count }}</h1>
  <div class="space-x-6 p-3">
    <button class="btn" @click="increase">Increase</button>
    <button class="btn" @click="decrease">Decrease</button>
  </div>
</template>

<script setup>
import { ref } from 'vue';

const count = ref(0);

const increase = () => {
  count.value += 1;
};

const decrease = () => {
  count.value -= 1;
};
</script>

<style lang="scss" scoped>
.btn {
  @apply bg-indigo-700 text-xl font-bold text-white px-6 py-3 rounded-md;
}
</style>
