---
layout: post
title: "map() & filter()"
---

**map & filter**

```ts
import { useState } from "react";

const App = () => {
  const fruits = ["orange", "fraise", "pomme"];

  const [selected, setSelected] = useState(
    new Array(fruits.length).fill(false)
  );

  const selectedFruits = selected
    .map((el, index) => (el ? fruits[index] : el))
    .filter((el) => el);

  return (
    <>
      <div>선택된 과일 : {selectedFruits.join(", ")} </div>
    </>
  );
};

export default App4;
```
