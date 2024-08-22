# react-app-vite

Simple React App using Vite

## Setup for macOS

### Nvm

`nvm` is node.js version manager.

```
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.7/install.sh | bash
```

Close and reopen terminal.

### Node.js

Install via `nvm`:

```bash
nvm install v20.15.1
```

Make sure you do not have default node set:

```bash
nvm unalias default
```

Activate node 20.15.1:

```bash
nvm use 20.15.1
```

### Configure npm

Configure `npm` (Node Package Manager) to save versions of packages in `packages.json`. This way you can have the same stable environment on all development machines:

```bash
nvm use 20.15.1
npm config set save=true
npm config set save-exact=true
```

## Development

### Configure Project

```bash
source configure.sh
```

### Run

Start `dev` server:

```bash
npm run dev
```

Open application in default browser:

```bash
open http://localhost:5173
```

### Build

Build (builds the app in `./dist`):

```bash
npm run build
```

Preview build (serves `./dist` on http://localhost:4173):

```bash
npm run preview
```

## How to create a new project

### Create project

```bash
npm create vite@latest . -- --template react
```

The `react` template provides a minimal setup to get React working in Vite with HMR and some ESLint rules.

### Configure HMR 

>  HMR === Hot Module Reloading

Currently, two official plugins are available, that can be used in `vite.config.js`:

- [@vitejs/plugin-react](https://github.com/vitejs/vite-plugin-react/blob/main/packages/plugin-react/README.md) uses [Babel](https://babeljs.io/) for Fast Refresh (used by default)
- [@vitejs/plugin-react-swc](https://github.com/vitejs/vite-plugin-react-swc) uses [SWC](https://swc.rs/) for Fast Refresh
