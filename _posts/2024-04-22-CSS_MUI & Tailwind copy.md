---
layout: post
title: "CSS_MUI & Tailwind"
---

**MUI**

<a> https://mui.com/material-ui/getting-started/installation/

In terminal

> npm install @mui/material @emotion/react @emotion/styled

In VS code

> copy the code Button

```ts
import { Button } from "@mui/material";

export default function Home() {
  return (
    <main>
      <Button variant="contained">Contained</Button>
    </main>
  );
}
```

### Customize Mui site

<a> https://bareynol.github.io/mui-theme-creator/

### Config in tailwind.config.js

```ts
/** @type {import('tailwindcss').Config} */
module.exports = {
  // avoid conflit with tailwind
  codePlugins: {
    preflight: false,
  },
  //
  important: true,
  prefix: "tw-",
  content: [
    "./src/pages/**/*.{js,ts,jsx,tsx,mdx}",
    "./src/components/**/*.{js,ts,jsx,tsx,mdx}",
    "./src/app/**/*.{js,ts,jsx,tsx,mdx}",
  ],
  theme: {
    extend: {
      backgroundImage: {
        "gradient-radial": "radial-gradient(var(--tw-gradient-stops))",
        "gradient-conic":
          "conic-gradient(from 180deg at 50% 50%, var(--tw-gradient-stops))",
      },
    },
  },
  plugins: [],
};
```

**Tailwind**

<a> https://tailwindcss.com/docs/installation

In terminal

> npm install -D tailwindcss
>
> npx tailwindcss init

**When there is a conflict**

```ts
<div className="text-red-300">Hello</div>
<div className="tw-text-red-300">Hello</div>
```

**Nomalize**

```ts
@tailwind base;
@tailwind components;
@tailwind utilities;

/* normalize */
body {
  margin: 0;
}
a {
  color: inherit;
  text-decoration: none;
}
blockquote,
dl,
dd,
h1,
h2,
h3,
h4,
h5,
h6,
hr,
figure,
p,
pre {
  margin: 0;
}
ol,
ul {
  list-style: none;
  margin: 0;
  padding: 0;
}
img,
svg,
video,
canvas,
audio,
iframe,
embed,
object {
  display: block;
  /* vertical-align: middle; */
}
img,
video {
  max-width: 100%;
  height: auto;
}
*,
::before,
::after {
  border-width: 0;
  border-style: solid;
  border-color: theme("borderColor.DEFAULT", currentColor);
}

```

### React Icons

<a>https://react-icons.github.io/react-icons/

> npm install react-icons --save

```js
import { FaBeer } from "react-icons/fa";

function Question() {
  return (
    <h3>
      Lets go for a <FaBeer />?
    </h3>
  );
}
```
