<script setup lang="ts"></script>

<template>
  <div class="relative min-h-dvh z-2 grid grid-rows-[1fr_max-content] gap-6">
    <div>
      <slot />
    </div>

    <LayoutFooter />

    <div
      class="absolute h-full inset-0 w-full pointer-events-none z-0 opacity-35"
    >
      <InspiraSnowfallBg
        color="ADD8E6"
        class="absolute inset-0"
        :min-radius="0.2"
        :max-radius="5"
        :speed="0.5"
      />
    </div>
  </div>
</template>
