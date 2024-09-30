---
layout: default
transition: fade
---

# Comentários

### Evite!

### Explique-se no código

```ts
// Verifica se o funcionário tem direito a todos os benefícios
if ((employee.flags && HOURLY_FLAG) && employee.age > 65) {
    //...
}
```

ou 


```ts
if (employee.isEligibleForFullBenefits()) {
    //...
}
```
* Codigo como comentário (remova)


---
layout: default
transition: fade
---

# Comentários

### O que não deve ser comentado
* Informações que podem ser rapidamente deduzidos a partir do próprio código
* "*Comentários-muleta*" que compensam códigos ruins. Melhor corrigir o código

<hr class="my-4"/>

### O que pode ser comentado (com cautela)
* Informações que explicam o **funcionamento** do código (comentário do diretor)
* Falhas, utilizando marcadores como `TODO:` ou `FIXME:`