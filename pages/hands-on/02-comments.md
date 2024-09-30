---
layout: default
---

<h1 v-mark.box.yellow class="w-fit px-4">Comentários</h1>


Use nomes que revelem seu propósito

````md magic-move
```java {2-13}
public static void main(String[] args) {
    Integer num = 1;
    switch (num) {
        case 1:
            num += 1;
            break;
        case 2:
            num += 2;
            break;
        default:
            break;
    }
    System.out.println(num);
}
```
```kotlin {2-8}
fun main() {
    var num = 1
    when (num) {
        1    -> num += 1
        2    -> num += 2
        else -> {}
    }
    println(num)
}
```
````