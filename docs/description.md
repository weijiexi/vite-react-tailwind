# Vite ReactApp 

## Structure

```
/vite-react-js
├── src 
│  ├── components
│  │   └── App.js
│  ├── index.html 
│  └── index.js
├── .gitignore 
├── package.json 
└── Readme.md
```

prepare the initial file: `src/index.html`, `src/index.js`, `src/components/App.js`:

`src/index.html`
```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="utf-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <title>Vite ReactApp</title>
  </head>
  <body>
    <div id="app"></div>
    <script type="module" src="index.js"></script>
  </body>
</html>
```

-   `src/index.js`

```js
import { createRoot } from "react-dom/client";
import { App } from "./components/App";

const container = document.getElementById("app");
const root = createRoot(container)
root.render(<App />);
```

-   `src/components/App.js`

```js
export function App() {
  return <h1>Hello world!</h1>;
}
```

- install react react-dom

```
npm i --save react react-dom  
```

- Add `"start"` scripts to the `package.json` file  

```
  "scripts": {
    "dev": "vite", // start dev server, aliases: `vite dev`, `vite serve`
    "build": "vite build", // build for production
    "preview": "vite preview" // locally preview production build
  },
```

- run react

```sh
npm dev
```

or

```sh
npx vite src/index.html
```