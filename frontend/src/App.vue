<script setup>
import { ref } from 'vue'

let counter = ref(0)

setInterval(() => {
  counter.value++
}, 1000)
</script>

<template>
  <div>
    <header class="bg-white shadow flex px-8 py-8" v-if="$route.meta.title">
      <img class="w-32 sm:w-64" src="./assets/logo.png" alt="">
    </header>
    <main>
      <router-view />
    </main>
  </div>
</template>
