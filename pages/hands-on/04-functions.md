---
layout: default
transition: fade
---

# Funções

<v-clicks>

* 1ª regra: Devem ser pequenas
* 2ª regra: Devem ser menores ainda!

</v-clicks>

<div v-click class="p-4 shadow bg-zinc-50 my-5 w-fit">
💡 Funções devem fazer somente uma coisa. Devem fazê-la bem. Devem fazer apenas ela.
</div>

<p v-click>O problema dessa declaração é que é difícil saber o que é <em v-mark>uma coisa</em>.</p>
<p v-click>Função <code>main()</code> executa o programa. É uma coisa!  <img src="/assets/troll.avif" class="w-10 inline"/></p>


<div v-click class="p-4 shadow bg-zinc-50 my-5 w-fit">
💡 Uma função faz mais de uma coisa se podemos extrair uma outra função de dentro dela que tenha significado por si só.
</div>
<div v-click class="p-4 shadow bg-zinc-50 my-5 w-fit">
💡 Uma função só deve operar num mesmo nível de abstração
</div>

---
layout: default
transition: fade
---

# Funções
Nível de abstração

<v-clicks>

* Cada função deve lidar com uma única camada de abstração. Ou seja, ela não deve misturar conceitos complexos e básicos dentro do mesmo escopo.
* Se uma função chama outras funções de alto nível, ela mesma deve estar no mesmo nível de abstração. Caso contrário, delegue operações de baixo nível para outras funções.

</v-clicks>

---
layout: default
transition: fade
---

# Funções
Nível de abstração

<div class="flex justify-between">

<div v-click>

```ts
function processOrder(order) {
  // Verifica se o pedido é válido
  if (order.items.length === 0) {
    throw new Error("Pedido inválido");
  }

  // Calcula o total do pedido
  let total = 0;
  for (let i = 0; i < order.items.length; i++) {
    total += order.items[i].price;
  }

  // Envia confirmação de pagamento
  sendConfirmation(order.customerEmail, total);
}
```
</div>

<div v-click>

```ts
function processOrder(order) {
  validateOrder(order);
  const total = calculateTotal(order.items);
  sendConfirmation(order.customerEmail, total);
}

function validateOrder(order) {
  if (order.items.length === 0) {
    throw new Error("Pedido inválido");
  }
}

function calculateTotal(items) {
  return items.reduce((sum, item) => sum + item.price, 0);
}
```
</div>

</div>

---
layout: default
transition: fade
---

# Funções
Parâmetros e retorno

<v-clicks>

- A quantidade ideal de parâmetros para uma função é zero
- Se não for possível, utilize 1 parâmetro
- Em casos mais específicos, utilize 2
- Como última opção, utilize 3
- Para mais de 3 deve-se ter um motivo muito especial
- Funções com retorno não podem ter side-effects
- Evite parâmetros booleanos

</v-clicks>

<div class="grid grid-cols-2 gap-8" v-click>

```ts
function setOpen(value: boolean) {
	isOpen = value;
}
```

```ts
function open() {
	isOpen = true;
}

function close() {
	isOpen = false;
}
```

</div>


---
layout: default
transition: fade
---

# Funções
Blocos try-catch

````md magic-move

```ts
function delete(page: Page) {
  try {
    deletePage(page);
    registry.deleteReference(page.name);
    configKeys.deleteKey(page.name.makeKey());
  } catch (Exception e) {
    logger.log(e.getMessage());
  }
}
```

```ts
function delete(page: Page) {
  try {
    deletePage(page);
    registry.deleteReference(page.name);
    configKeys.deleteKey(page.name.makeKey());
  } catch (Exception e) {
    logger.log(e.getMessage());
  }
}

private function deletePageAndAllReferences(page: Page) throws Exception {
  // ...
}

private function logError(Exception e) {
  // ...
}
```

```ts
function delete(page: Page) {
  try {
   deletePageAndAllReferences(page);
  } catch (Exception e) {
    logError();
  }
}

private function deletePageAndAllReferences(page: Page) throws Exception {
  deletePage(page);
  registry.deleteReference(page.name);
  configKeys.deleteKey(page.name.makeKey());
}

private function logError(Exception e) {
  logger.log(e.getMessage());
}
```

````