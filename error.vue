<script setup lang="ts">
const handleError = () => clearError({ redirect: "/" })
</script>

<template>
  <div class="flex flex-col items-center justify-center space-y-2 min-h-dvh">
    <InspiraHyperText text="404" class="text-8xl font-bold" :duration="800" />
    <InspiraHyperText
      text="Página não encontrada"
      class="text-2xl lg:text-4xl font-bold"
      :duration="800"
    />

    <div class="pt-4">
      <Button @click="handleError">Voltar ao início</Button>
    </div>
  </div>
</template>
