---
layout: default
---

# Os dois valores do software

<div class="flex gap-4">
  <div class="shadow p-4 bg-gray-50">
    <h3 v-click class="mb-4">☝️ Comportamento</h3>
    <ul>
      <li v-click>funcionalidades</li>
      <li v-click>é que faz os clientes ganharem ou economizarem dinheiro</li>
    </ul>
  </div>

  <div class="shadow p-4 bg-gray-50">
    <h3 v-click class="mb-4">✌️ Estrutura</h3>
    <ul>
      <li v-click>arquitetura</li>
      <li v-click>é o que mantêm o comportamento de pé sem colapsar</li>
    </ul>
  </div>
</div>

<div class="h-full relative mt-10">
<ul>
  <li v-click><span class="font-bold">Clientes</span> precisam</li>
  <li v-click><span class="font-bold">Usuários</span> enxergam</li>
  <li v-click><span class="font-bold">Vendedores</span> prometem</li>
  <li v-click><span class="font-bold">POs</span> gerenciam</li>
  <li v-click><span class="font-bold">QAs</span> validam</li>
  <li v-click v-motion :initial="{x: 0}" :click-13="{x: 350, transition: {stiffness: 100}}" v-mark.box.white="{at: 13}"><span class="font-bold">Devs</span> implementam</li>
</ul>
  <div v-click class="absolute h-40 w-1 -top-4 left-108 border-l-2 border-zinc-400 border-dashed"/>
</div>

---
layout: center
transition: fade
---

<Arrow x1="50%" y1="10%" x2="50%" y2="90%" two-way />
<Arrow x1="90%" y1="50%" x2="10%" y2="50%" two-way />

<span class="absolute top-[48%] left-10">- Limpo</span>
<span class="absolute top-[48%] right-10">+ Limpo</span>
<span class="absolute top-[5%] left-[47%]">Funciona</span>
<span class="absolute bottom-[4%] left-[46%]">Não Funciona</span>

<div class="absolute bottom-4 right-4 flex flex-col text-sm bg-zinc-50 p-2 shadow text-zinc-500">
<p class="!my-0">x: estrutura</p>
<p class="!my0">y: comportamento</p>
</div>
  
<!-- <img src="/assets/dog-fire.gif" class="absolute left-30" v-click/> -->
<div class="bg-yellow" v-if="$clicks <= 4">
  <img src="/assets/mr-incredible/happy.webp" class="absolute left-[60%] top-16 size-48" v-click/>
  <img src="/assets/mr-incredible/neutral.webp" class="absolute left-[20%] top-16 size-48" v-click/>
  <img src="/assets/mr-incredible/uncanny.webp" class="absolute left-[20%] top-76 size-48" v-click/>
  <img src="/assets/mr-incredible/work.gif" class="absolute left-[55%] top-76 h-48" v-click/>
</div>

---
layout: center
transition: fade
---

<Arrow x1="50%" y1="10%" x2="50%" y2="90%" two-way />
<Arrow x1="90%" y1="50%" x2="10%" y2="50%" two-way />

<span class="absolute top-[48%] left-10">- Limpo</span>
<span class="absolute top-[48%] right-10">+ Limpo</span>
<span class="absolute top-[5%] left-[47%]">Funciona</span>
<span class="absolute bottom-[4%] left-[46%]">Não Funciona</span>

  <!-- <Arrow x1="10" y1="10" x2="160" y2="10" class="text-green-600" /> -->
<div v-click class="absolute top-4 left-4 text-sm bg-zinc-50 p-2 shadow text-zinc-500 w-fit h-fit flex flex-col">
  <span class="text-green-600">melhoria/bugfix</span>
  <span class="text-red-600">bug</span>
  <span class="text-blue-600">refatoração</span>
</div>

<v-drag-arrow v-click pos="161,194,0,-83" class="text-green-600"/>
<v-drag-arrow v-click pos="204,176,0,75" class="text-red-600"/>
<v-drag-arrow v-click pos="138,323,90,1" class="text-blue-600"/>

<v-drag-arrow v-click pos="761,194,0,-83" class="text-green-600"/>
<v-drag-arrow v-click pos="449,346,0,-83" class="text-green-600"/>

<div class="absolute bottom-4 right-4 flex flex-col text-sm bg-zinc-50 p-2 shadow text-zinc-500">
<p class="!my-0">x: estrutura</p>
<p class="!my0">y: comportamento</p>
</div>
