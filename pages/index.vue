<script setup lang="ts">
import { PinIcon } from "lucide-vue-next"

useSeoMeta({
  title: "Meus links - pedroruviaro",
})

const links = [
  {
    text: "GitHub",
    href: "https://github.com/pedrodruviaro",
  },
  {
    text: "LinkedIn",
    href: "https://www.linkedin.com/in/pedroruviaro/",
  },
  {
    text: "Site Pessoal",
    href: "https://pedroruviaro.com.br/",
  },
  {
    text: "Blog",
    href: "https://pedroruviaro.com.br/notes",
  },
  {
    text: "Conheça a wire",
    href: "https://www.wire.art.br/",
  },
  {
    text: "Email",
    href: "mailto:pedrodruviaro@gmail.com",
  },
]

const handleNavigation = (href: string) => {
  if (!window) return

  window.open(href, "_blank")
}
</script>

<template>
  <div class="relative min-h-dvh z-2 grid grid-rows-[1fr_max-content] gap-6">
    <main class="container pt-12 pb-4 lg:pt-20">
      <section class="flex justify-center mb-4">
        <Avatar size="lg">
          <AvatarImage
            src="https://avatars.githubusercontent.com/u/82953655?v=4"
            alt="@pedrodruviaro"
          />
        </Avatar>
      </section>

      <section class="mb-10 flex justify-center text-center flex-col gap-4">
        <p class="text-white/80 max-w-[32ch] mx-auto">
          Enhenheiro de software em formação e desenvolvedor front-end
        </p>

        <p class="flex items-center justify-center gap-2 text-white/80">
          <PinIcon />
          <span class="font-semibold"> Rio Grande do Sul, Brasil </span>
        </p>
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

    <footer class="py-4">
      <p class="text-sm text-center text-white/60">
        Feito com carinho 💜 -
        <NuxtLink
          to="https://pedroruviaro.com.br/"
          target="_blank"
          class="underline"
          >pedroruviaro.com.br</NuxtLink
        >
      </p>
    </footer>

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
