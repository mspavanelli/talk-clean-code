---
layout: default
transition: fade
---

# Nomes
Use nomes que revelem seu propósito


<div v-click class="w-80">
```ts
let d = 10; // days since creation
```
</div>
<div v-click class="w-80">
```ts
let daysSinceCreation = 10;
```
</div>


---
layout: two-cols
transition: fade
---

# Nomes
Use nomes que revelem seu propósito

````md magic-move
```java
public List<int[]> getThem() {
  List<int[]> list1 = new ArrayList<int[]>();
  for (int[] x : theList) {
    if (x[0] == 4) {
      list.add(x);
    }
  }
  return list1;
}
```

```java
public List<int[]> getFlaggedCells() {
  List<int[]> flaggedCells = new ArrayList<int[]>();
  for (int[] cell : gameBoard) {
    if (cell[STATUS_VALUE] == FLAGGED) {
      flaggedCells.add(cell);
    }
  }
  return flaggedCells;
}
```

```java
public List<Cell> getFlaggedCells() {
  List<Cell> flaggedCells = new ArrayList<Cell>();
  for (Cell cell : gameBoard) {
    if (cell.isFlagged()) {
      flaggedCells.add(cell);
    }
  }
  return flaggedCells;
}
```
````

::right::

<div class="mt-22 ml-4" v-click="3">

```java
public List<int[]> getThem() {
  List<int[]> list1 = new ArrayList<int[]>();
  for (int[] x : theList) {
    if (x[0] == 4) {
      list.add(x);
    }
  }
  return list1;
}
```

</div>

---
layout: default
transition: fade
---

# Nomes
Use nomes passíveis de busca

<div v-click>
```ts
for (int j = 0; j < 34; j++) {
  s += (t[j]*4)/5;
}
```
</div>

<div v-click>
```ts
const NUMBER_OF_TASKS = 34;
const realDaysPerIdealDay = 4;
const WORK_DAYS_PER_WEEK = 5;
for (let j = 0; j < NUMBER_OF_TASKS; j++) {
  const adjustedValue = (taskEstimate[j] * realDaysPerIdealDay) / WORK_DAYS_PER_WEEK;
  sum += adjustedValue;
}
```
</div>


---
layout: default
transition: fade
---

# Nomes
Evite nomes genéricos

````md magic-move
```ts
let tmp: string = user.name();
tmp += " " + user.phone.number();
tmp += " " + user.email();

// ...

template.set("user_info", tmp);
```
```ts
let user_info: string = user.name();
user_info += " " + user.phone.number();
user_info += " " + user.email();

// ...

template.set("user_info", user_info);
```
````

---
layout: default
transition: fade
---

# Nomes
Inclua informações úteis

````md magic-move
```ts
let id: string; // Exemplo: "af84ef845cd8"
```
```ts
let hex_id: string;
```
````

---
layout: default
transition: fade
---

# Nomes
O tamanho do nome é proporcional ao escopo

* `i` para iteradores em loops
* variáveis que existem somente num método ou classe podem aproveitar do contexto
* variáveis globais precisam ter nomes mais específicos para compensar seu alcance

---
layout: default
transition: fade
---

# Nomes
Não adicione contexto desnecessário

````md magic-move
```ts
class Person {
  private personName: string;
  private personDocument: string;
  private personBirthday: string;
}
```

```ts
class Person {
  private name: string;
  private document: string;
  private birthday: string;
}
```
````

Remova ambiguidade

gg