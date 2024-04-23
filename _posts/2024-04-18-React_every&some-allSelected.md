---
layout: post
title: "every() & some()"
---

**every()**

```ts
const array = [1, 30, 39, 29, 10, 13];
console.log(array.every((value) => value < 40));
// Expected output: true
```

> All select checkbox

```ts
import { useState } from "react";

const App = ()={
  const mainMenus = [
         '후라이드',
         '양념',
         '간장',
         '닭강정(소)',
         '닭강정(중)',
         '닭강정(대)',
         '숯불구이',
         '치즈볼',
      ]

  const [optionCheckeds, setOptionCheckeds] = useState(
    new Array(mainMenus.length).fill(false)
  )

  const toggleOptionCheck = () => {
      const newOptionCheckeds = optionCheckeds.map((el, _index) =>
        index === _index ? !el : el
      )
      setOptionCheckeds(newOptionCheckeds)
  }

  const btnAllChecked = optionCheckeds.every((el) => el);

  const toggleAllchecked = () => {
    if (btnAllChecked) {
      const newOptionCheckeds = optionCheckeds.map((el) => false);
      setOptionCheckeds(newOptionCheckeds);
    } else {
      const newOptionCheckeds = optionCheckeds.map((el) => true);
      setOptionCheckeds(newOptionCheckeds);
    }
  };

return (
  <div>
    <div onClick={toggleAllchecked}>
      {btnAllChecked ? '[✓]' : '[  ]'} 전체 선택
    </div>
    <ul>
      {mainMenus.map((option, index) => (
          <li key={index}
            onClick={() => toggleOptionCheck(index)}
            >
            {optionCheckeds[index] ? '[✓]' : '[  ]'}
            &nbsp;
            {option}
          </li>
      ))}
    </ul>
  </div>
  )
}
```

**some()**

```ts
const array = [1, 2, 3, 4, 5];
const even = (element) => element % 2 === 0;

console.log(array.some(even));
// Expected output: true
```
