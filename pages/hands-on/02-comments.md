---
layout: default
transition: fade
---

# Comentários

<h2 v-click v-mark.highlight.yellow class="w-fit px-2 py-1">Evite!</h2>

<h4 v-click class="mt-6">Explique-se no código</h4>

<div v-click>
```ts
// Verifica se o funcionário tem direito a todos os benefícios
if ((employee.flags && HOURLY_FLAG) && employee.age > 65) {
    //...
}
```
</div>

<div v-click>
ou 


```ts
if (employee.isEligibleForFullBenefits()) {
    //...
}
```
</div>

<p v-click>Comentários muitas vezes servem para compensar a falta de expressividade do código.</p>


---
layout: default
transition: fade
---

# Comentários

### O que não deve ser comentado
* Informações que podem ser rapidamente deduzidos a partir do próprio código
* "*Comentários-muleta*" que compensam códigos ruins. Melhor corrigir o código
* Código morto ou que talvez será usado (controle de versão serve para isso)

<hr class="my-4"/>

### O que pode ser comentado (com cautela)
* Informações que explicam o **funcionamento** do código (comentário do diretor)
```py
# remove tudo depois do segundo '*'
name = '*'.join(line.split('*')[:2])
```

* Falhas, utilizando marcadores como `TODO:` ou `FIXME:`