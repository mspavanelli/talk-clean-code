---
layout: default
transition: fade
---

# Object Calisthenics



---
layout: default
transition: fade
---

# Object Calisthenics

<ul class="space-y-4">
  <li v-mark.highlight.yellow class="w-fit">Não use abreviações</li>
  <li v-mark.highlight.yellow class="w-fit">Um nível de identação por método</li>
  <li v-mark.highlight.yellow class="w-fit">Mantenha as entidades pequenas</li>
  <li v-mark.highlight.yellow class="w-fit">Não utilize `else` (fail fast)</li>
  <li>Coleções como classes</li>
  <li>1 ponto por linha</li>
  <li>Classes com no máximo 2 variáveis</li>
  <li>Envolva tipos primitivos em strings e classes</li>
  <li>Não usar getters e setters</li>
</ul>

---
layout: default
transiton: fade
---

# Object Calisthenics
Fail Fast

<div class="overflow-scroll max-h-[80%]">
```ts
function processOrder(order) {
  // Check if the order exists
  if (order) {
    // Check if the order has a customer
    if (order.customer) {
      // Check if the customer is active
      if (order.customer.active) {
        // Check if the order has items
        if (order.items && order.items.length > 0) {
          // Check if the payment is confirmed
          if (order.payment.confirmed) {
            // Process the order
            console.log("Order successfully processed.");
          } else {
            console.log("Payment not confirmed.");
          }
        } else {
          console.log("The order has no items.");
        }
      } else {
        console.log("Inactive customer.");
      }
    } else {
      console.log("Order without a customer.");
    }
  } else {
    console.log("Invalid order.");
  }
}
```
</div>

---
layout: default
transiton: fade
---

# Object Calisthenics
Fail Fast

<div class="overflow-scroll max-h-[90%]">
```ts
function processOrder(order) {
  if (!order) {
    console.log("Invalid order.");
    return;
  }
  if (!order.customer) {
    console.log("Order without a customer.");
    return;
  }
  if (!order.customer.active) {
    console.log("Inactive customer.");
    return;
  }
  if (!order.items || order.items.length === 0) {
    console.log("The order has no items.");
    return;
  }
  if (!order.payment.confirmed) {
    console.log("Payment not confirmed.");
    return;
  }
  console.log("Order successfully processed.");
}
```
</div>