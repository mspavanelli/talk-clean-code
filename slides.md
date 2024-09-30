---
theme: default
title: Clean Code
image: ./assets/cover.webp
drawings:
  persist: false
transition: slide-left
fonts:
  provider: google
  sans: Neucha
---

<img src="/assets/cover.webp" class="absolute top-0 left-0" v-motion :initial="{x: 0}" :click-1='{x: 500, transition: {duration: 750}}' :leave='{x: 0}'/>

<div class="h-full w-1/2 flex flex-col justify-between">
  <header>
    <h1 v-click="2">Clean Code</h1>
    <p v-click="3">A Arte de Escrever Programas Legíveis</p>
  </header>
  <div v-motion :initial="{scale: 0, y: 20}" :click-4="{scale: 1, y: 0}" class="w-fit">
    <p class="!mt-0 !mb-1">Matheus <span class="font-bold" v-mark="{at: 5}">Pavanelli</span></p>
    <p class="!my-0 text-sm text-zinc-500">Desenvolvedor Web</p>
  </div>
</div>

---
src: ./pages/prologue/index.md
---

---
src: ./pages/definitions/index.md
---


---
src: ./pages/hands-on/index.md
---
