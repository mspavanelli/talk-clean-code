---
layout: default
---

# Os dois valores do software

<div class="flex gap-4">
  <div class="shadow p-4 bg-gray-50">
    <h3 v-click class="mb-4">☝️ Comportamento</h3>
    <ul>
      <li v-click>* funcionalidades</li>
      <li v-click>* é que faz os clientes ganharem ou economizarem dinheiro</li>
    </ul>
  </div>

  <div class="shadow p-4 bg-gray-50">
    <h3 v-click class="mb-4">✌️ Estrutura</h3>
    <ul>
      <li v-click>* arquitetura</li>
      <li v-click>* é o que mantêm o comportamento de pé sem colapsar</li>
    </ul>
  </div>
</div>

<div class="h-full relative">
  <p class="absolute top-5 left-10" v-click><span class="font-bold">Clientes</span> precisam</p>
  <p class="absolute top-10 left-70" v-click><span class="font-bold">Usuários</span> enxergam</p>
  <p class="absolute top-20 left-40" v-click><span class="font-bold">Vendedores</span> prometem</p>
  <p class="absolute top-40 left-20" v-click><span class="font-bold">POs</span> gerenciam</p>
  <p class="absolute top-60 left-60" v-click><span class="font-bold">QAs</span> validam</p>
  <p class="absolute top-30 left-90" v-click><span class="font-bold">Devs</span> implementam</p>

  <div v-click class="absolute h-80 w-1 top-2 left-110 border-l-2 border-zinc-500 border-dashed"/>
</div>

---
layout: center
---

<Arrow x1="50%" y1="10%" x2="50%" y2="90%" two-way />
<Arrow x1="90%" y1="50%" x2="10%" y2="50%" two-way />
<Arrow x1="10" y1="10" x2="160" y2="10" class="text-green-600" />
<span class="text-green-600 absolute top-10 left-10">refatoração</span>

<span class="absolute top-[48%] left-10">- Limpo</span>
<span class="absolute top-[48%] right-10">+ Limpo</span>
<span class="absolute top-[5%] left-[47%]">Funciona</span>
<span class="absolute bottom-[4%] left-[46%]">Não Funciona</span>

<div class="absolute bottom-4 right-4 flex flex-col text-sm bg-zinc-50 p-2 shadow text-zinc-500">
<p class="!my-0">x: estrutura</p>
<p class="!my0">y: comportamento</p>
</div>
  
<img src="/assets/dog-fire.gif" class="absolute left-30"/>
<img src="/assets/mr-incredible-happy.webp" class="absolute left-[60%] top-16 size-48"/>
