<script setup lang="ts">
useHead({
  titleTemplate: (title) => {
    return title ? `${title} - pedroruviaro` : "pedroruviaro"
  },
})
</script>

<template>
  <NuxtLayout>
    <NuxtPage />
  </NuxtLayout>
</template>
