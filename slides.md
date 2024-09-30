---
theme: default
title: "slidev tutorial"
background: ./assets/abstract.avif
transition: slide-left
fonts:
  sans: Nunito
---

# Clean Code

A arte de escrever programas legíveis

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
---

Extraia os blocos try/catch

````md magic-move
```ts
function delete(page: Page) {
  try {
    deletePage(page);
    registry.deleteReferenece(page.name);
    config.keys.deleteKeys(page.name.makeKey());
  } catch (Excepetion e) {
    logger.log(e.getMessage());
  }
}
```

```ts
function delete(page: Page) {
  try {
    deletePage(page);
    registry.deleteReferenece(page.name);
    config.keys.deleteKeys(page.name.makeKey());
  } catch (Excepetion e) {
    logger.log(e.getMessage());
  }
}

function deletePageAndAllReferences(page: Page) throws Exception {

}

function logError(Exception e) {

}
```

```ts
function delete(page: Page) {
  try {

  } catch (Excepetion e) {

  }
}

function deletePageAndAllReferences(page: Page) throws Exception {
  deletePage(page);
  registry.deleteReferenece(page.name);
  config.keys.deleteKeys(page.name.makeKey());
}

function logError(Exception e) {
  logger.log(e.getMessage());
}
```

```ts
function delete(page: Page) {
  try {
    deletePageAndAllReferences(page);
  } catch (Excepetion e) {
    logError(e);
  }
}

function deletePageAndAllReferences(page: Page) throws Exception {
  deletePage(page);
  registry.deleteReferenece(page.name);
  config.keys.deleteKeys(page.name.makeKey());
}

function logError(Exception e) {
  logger.log(e.getMessage());
}
```
````

---
layout: default
---

````md magic-move
```ts
let d = 10; // days since creation
```

```ts
let daysSinceCreation = 10;
```
````

---
layout: statement
---

<div class="w-160 mx-auto">
  <em class="text-xl">"Qualquer um consegue escrever código que um computador entende. Bons programadores escrevem código que humanos entendem"</em>
  <p class="text-right text-gray-500">Martin Fowler</p>
</div>
