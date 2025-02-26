<script setup lang="ts">
import { PinIcon } from "lucide-vue-next"

const links = [
  {
    text: "GitHub",
    href: "https://github.com/pedrodruviaro",
  },
  {
    text: "LinkedIn",
    href: "https://github.com/pedrodruviaro",
  },
  {
    text: "Site",
    href: "https://pedroruviaro.com.br/",
  },
  {
    text: "Blog",
    href: "https://pedroruviaro.com.br/notes",
  },
]

const handleNavigation = (href: string) => {
  if (!window) return

  window.open(href, "_blank")
}
</script>

<template>
  <div class="relative min-h-screen z-2">
    <main class="container py-20">
      <section class="flex justify-center mb-4">
        <Avatar size="lg">
          <AvatarImage
            src="https://avatars.githubusercontent.com/u/82953655?v=4"
            alt="@pedrodruviaro"
          />
          <AvatarFallback>PD</AvatarFallback>
        </Avatar>
      </section>

      <section class="mb-10 flex justify-center text-center flex-col gap-2">
        <p class="flex items-center justify-center gap-2">
          <PinIcon />
          <span> Rio Grande do Sul, Brasil </span>
        </p>

        <p>Enhenheiro de software de desenvolvedor front-end</p>
      </section>

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

    <div
      class="absolute h-full inset-0 w-full pointer-events-none z-0 opacity-40"
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
