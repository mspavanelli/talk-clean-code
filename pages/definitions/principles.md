---
layout: two-cols
---

<h1 v-mark.box class="w-fit p-4">Princípios</h1>

<ul class="list-unset space-y-8 mt-14">
  <li v-click class="flex items-center gap-2"><PhArrowRight :size="4" /> Simplicidade</li>
  <li v-click class="flex items-center gap-2"><PhArrowRight :size="4" /> Testes automatizados</li>
  <li v-click class="flex items-center gap-2 w-fit" v-mark.highlight.yellow><PhArrowRight :size="4" /> Refatoração</li>
</ul>

::right::

<div class="h-full flex items-center">
<blockquote v-motion :initial='{scale: 0}' :click-7='{scale: 1, transition: {duration: 300}}' class="block my-auto mx-auto">
<p class="text-lg">“Refatoração é o processo de modificar um sistema de software visando melhorar sua <span v-mark.box.red="{at: 8}">estrutura</span> interna de modo que não altere o <span v-mark.box.blue="{at: 9}">comportamento</span> externo do código.”</p>

(Martin Fowler)
</blockquote>
</div>