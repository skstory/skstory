---
layout: post
title: "new Array() & fill()"
---

**new Array**

```js
new Array();
new Array(element1);
new Array(element1, element2);
new Array(arrayLength);
```

```js
const menu = "[a, b, c, d]";
console.log(new Array(menu.length));
// Expected output: [vide × 4]
```

**fill()**

```js
const array1 = [1, 2, 3, 4];

// Fill with 0 from position 2 until position 4
console.log(array1.fill(0, 2, 4));
// Expected output: Array [1, 2, 0, 0]

// Fill with 5 from position 1
console.log(array1.fill(5, 1));
// Expected output: Array [1, 5, 5, 5]

console.log(array1.fill(6));
// Expected output: Array [6, 6, 6, 6]
```

**new Array + fill()**

```js
const newArray = new Array(4).fill(true);
console.log(newArray);
// Expected output: [ true, true, true, true]
```
