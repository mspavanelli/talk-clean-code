---
layout: two-cols-header
transition: fade
---

# Nomes
Use nomes que revelem seu propósito

::left::


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

::right::

<div v-click>
```java
public List<int[]> getThem() {
  List<int[]> list1 = new ArrayList<int[]>();
  for (int[] x : theList) {
    if (x[0] == 4) {
      list1.add(x);
    }
  }
  return list1;
}
```
</div>


<div v-click>
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
</div>

---
transition: slide-up
layout: two-cols
---

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
public List<int[]> getFlaggedCells() {
  List<int[]> flaggedCells = new ArrayList<int[]>();
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

<div class="mt-14 ml-4" v-click="4">

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

### Use nomes passíveis de busca

gg

---
layout: default
transition: fade
---

# Nomes

### Não adicione contexto desnecessário

gg

---
layout: default
transition: fade
---

# Nomes

### Evite nomes genéricos

gg

---
layout: default
transition: fade
---

# Nomes

### Inclua informações úteis

gg

---
layout: default
transition: fade
---

# Nomes

### O tamanho do nome é proporcional ao escopo

gg

---
layout: default
transition: fade
---

# Nomes

### Remova ambiguidade

gg