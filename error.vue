<script setup lang="ts">
useSeoMeta({
  title: "Página não encontrada - pedroruviaro",
})

const handleError = () => clearError({ redirect: "/" })
</script>

<template>
  <NuxtLayout>
    <div
      class="flex flex-col items-center justify-center space-y-2 container mt-40 lg:mt-60"
    >
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
  </NuxtLayout>
</template>
