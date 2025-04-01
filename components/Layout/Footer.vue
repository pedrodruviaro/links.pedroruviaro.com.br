<script setup lang="ts">
const currentYear = computed(() => new Date().getFullYear())
</script>

<template>
  <footer class="py-4">
    <p class="text-sm text-center text-white/50">
      {{ currentYear }} -
      <NuxtLink
        to="https://pedroruviaro.com.br/"
        target="_blank"
        class="hover:underline"
        >pedroruviaro.com.br</NuxtLink
      >
    </p>
  </footer>
</template>
