# Nuxt 3 Minimal Starter with Vuetify3

## How to setup this repository

```bash
# create nuxt3 project
npx nuxi init <your-app-name>

cd <your-app-name>

yarn install

# install Vuetify3
yarn add vuetify@next mdi

yarn add -D sass
```

## Modify nuxt.config.ts

```typescript
// https://v3.nuxtjs.org/api/configuration/nuxt.config
export default defineNuxtConfig({
  rootDir: './src',
  css: ["vuetify/lib/styles/main.sass", "mdi/css/materialdesignicons.min.css"],
  build: {
    transpile: ["vuetify"],
  },
  vite: {
    define: {
      "process.env.DEBUG": false,
    },
  },
});
```

## Start Development Server

```bash
yarn dev
```
