<script setup lang="ts">
import { links } from "~/constants/links"

useSeoMeta({
  title: "Links",
})

const handleNavigation = (href: string) => {
  if (!window) return

  window.open(href, "_blank")
}
</script>

<template>
  <main class="container pt-12 pb-4 lg:pt-20">
    <HomeAvatarSection class="mb-4" />

    <HomeTextInfosSection class="mb-10" />

    <div class="flex flex-col gap-4 max-w-60 mx-auto">
      <InspiraInteractiveHoverButton
        class="w-full"
        v-for="link in links"
        :key="link.text"
        :href="link.href"
        :text="link.text"
        @click="() => handleNavigation(link.href)"
      />
    </div>
  </main>
</template>
