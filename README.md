# ReactTS 18 with Tailwind CSS, ESLint, Prettier and Vite

[![Commitizen friendly](https://img.shields.io/badge/commitizen-friendly-brightgreen.svg)](http://commitizen.github.io/cz-cli/)

This is a [React](https://react.dev) + [TypeScript](https://www.typescriptlang.org/) + [Tailwind CSS](https://tailwindcss.com) boilerplate to be built with [Vite](https://vitejs.dev). It also includes [ESLint 8](https://eslint.org), [Vitest](https://vitest.dev), [Husky](https://typicode.github.io/husk) and a pre-commit hook that runs `prettier --write` and `eslint --fix`.

## What's inside?

- [Vite](https://vitejs.dev)
- [React 18](https://react.dev)
- [TypeScript](https://www.typescriptlang.org)
- [@vitejs/plugin-react-swc](https://github.com/vitejs/vite-plugin-react-swc) uses [SWC](https://swc.rs/) for Fast Refresh
- [ESLint 8](https://eslint.org)
  - [eslint-plugin-react](https://github.com/jsx-eslint/eslint-plugin-react)
  - [eslint-plugin-react-hooks](https://www.npmjs.com/package/eslint-plugin-react-hooks)
  - [eslint-plugin-react-refresh](https://www.npmjs.com/package/eslint-plugin-react-refresh)
  - [typescript-eslint](https://typescript-eslint.io)
  - [eslint-plugin-tailwindcss](https://github.com/francoismassart/eslint-plugin-tailwindcss)
- [@tanstack/react-router](https://tanstack.com/router/latest)
- [@tanstack/react-query](https://tanstack.com/query/latest)
- [@tanstack/react-table](https://tanstack.com/table/latest)
- [Tailwind CSS](https://tailwindcss.com)
- [shadcn/ui](https://ui.shadcn.com/)
- [Zod](https://zod.dev/)
- [lucide](https://lucide.dev)
- [Vitest](https://vitest.dev)
- [Prettier](https://prettier.io)
- [Husky](https://typicode.github.io/husky/)

---

## Getting Started

### Install

Install dependencies.

```bash
yarn
```

Serve with hot reload at <http://localhost:{PORT}>.

```bash
yarn dev
```

### Other Commands

#### Prettier

```bash
yarn format
```

#### Lint

Run ESLint

```bash
yarn lint
```

Run ESLint and fix

```bash
yarn lint:fix
```

#### Build

```bash
yarn build
```

#### Test

```bash
yarn test
```

#### Commit commands

This project will use [commitlint](https://commitlint.js.org) to ensure that commit messages are [Conventional Commits specification](https://www.conventionalcommits.org) compliants.

To help you build more efficient commit messages, you will use the [commitizen](https://github.com/commitizen/cz-cli) package by running this command :

```bash
yarn cz
```

---

## shadcn/ui

### Adding Components

[Beautifully designed components](https://ui.shadcn.com/docs) that you can copy and paste into your apps. Accessible. Customizable. Open Source.

```bash
npx shadcn-ui@latest add button
```

### Adding new colors

To add new colors, you need to add them to your CSS file and to your `tailwind.config.js` file. [More info](https://ui.shadcn.com/docs/theming#adding-new-colors)

app/globals.css

```css
:root {
  --warning: 38 92% 50%;
  --warning-foreground: 48 96% 89%;
}

.dark {
  --warning: 48 96% 89%;
  --warning-foreground: 38 92% 50%;
}
```

tailwind.config.js

```js
module.exports = {
  theme: {
    extend: {
      colors: {
        warning: "hsl(var(--warning))",
        "warning-foreground": "hsl(var(--warning-foreground))",
      },
    },
  },
};
```

You can now use the warning utility class in your components.

```html
<div className="bg-warning text-warning-foreground" />
```

---

## Recommended VS Code extensions

- [ESLint](https://marketplace.visualstudio.com/items?itemName=dbaeumer.vscode-eslint)
- [Prettier](https://marketplace.visualstudio.com/items?itemName=esbenp.prettier-vscode)

## Husky

Workaround for [Node Version Managers and GUIs](https://typicode.github.io/husky/how-to.html#node-version-managers-and-guis)

```sh
# ~/.config/husky/init.sh

export NVM_DIR=~/.nvm

#source $(brew --prefix nvm)/nvm.sh # This loads nvm with brew.sh
[ -s "$NVM_DIR/nvm.sh" ] && \. "$NVM_DIR/nvm.sh" # or this loads nvm

#exit 1 # test hook without committing
```

## ESLint version 9+

- [Tracking: Flat Config support](https://github.com/eslint/eslint/issues/18093)

### Open issues

- [eslint-plugin-react-hooks & "Flat Config" (ESLint 9) #28313](https://github.com/facebook/react/issues/28313)
- [-BUG- Support eslint's new config file (flat) for recommended rules #280](https://github.com/francoismassart/eslint-plugin-tailwindcss/issues/280)
