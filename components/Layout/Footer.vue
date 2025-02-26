<script setup lang="ts">
const currentYear = computed(() => new Date().getFullYear())
</script>

<template>
  <footer class="py-4">
    <p class="text-sm text-center text-white/60">
      {{ currentYear }} - Feito com carinho 💜
      <NuxtLink
        to="https://pedroruviaro.com.br/"
        target="_blank"
        class="underline"
        >pedroruviaro.com.br</NuxtLink
      >
    </p>
  </footer>
</template>
