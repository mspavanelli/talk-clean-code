---
layout: two-cols
transition: slide-up
---

# Princípios

<ul class="list-unset space-y-8 mt-14">
  <li v-click class="flex items-center gap-2"><PhArrowRight :size="4" /> Simplicidade na comunicação</li>
  <li v-click class="flex items-center gap-2"><PhArrowRight :size="4" /> Testes automatizados</li>
  <li v-click class="flex items-center gap-2 w-fit" v-mark.highlight.yellow><PhArrowRight :size="4" /> Refatoração</li>
</ul>

::right::

  <blockquote v-motion :initial='{scale: 0}' :click-6='{scale: 1, transition: {duration: 300}}' class="block mt-12 mx-auto">
    <p class="text-lg">“Refatoração é uma modificação feita na <span v-mark.box.red="{at: 7}">estrutura</span> interna do software para deixá-lo mais fácil
    de compreender e menos custoso para alterar, sem que seu <span v-mark.box.blue="{at: 8}">comportamento</span> observável seja alterado.”</p>
    <span class="text-right block text-gray">Martin Fowler</span>
  </blockquote>

 <div class="mt-12" v-mark.bracket.white="{at: 9}" v-motion :initial="{scale: 0.9, y: 10, opacity: 0}" :click-9="{scale: 1, y: 0, opacity: 1}">💡 <b>Estrutura</b> e <b>comportamento</b> são os dois valores de um software!</div>