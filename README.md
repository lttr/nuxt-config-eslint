# Eslint config for Nuxt

An opinionated Eslint config for Nuxt apps.

## What's included

This config extends `@nuxt/eslint` module with additional packages:

- [eslint-plugin-vue-scoped-css](https://github.com/future-architect/eslint-plugin-vue-scoped-css) - scoped CSS best practices
- [eslint-plugin-vuejs-accessibility](https://vue-a11y.github.io/eslint-plugin-vuejs-accessibility/) - a11y rules
- [eslint-config-prettier](https://github.com/prettier/eslint-config-prettier) - disable rules conflicting with Prettier

Plus opinionated Vue rules:

- `vue/block-lang` - enforce TypeScript in script blocks
- `vue/block-order` - enforce template/script/style order
- `vue/component-api-style` - enforce `<script setup>`
- `vue/define-props-declaration` - enforce type-based props
- `vue/component-name-in-template-casing` - PascalCase components
- `vue/require-typed-ref` - typed ref() calls
- `vue/v-for-delimiter-style` - enforce `of` over `in`
- `vue/v-bind-style` - enforce `:foo` shorthand over `:foo="foo"`

## Usage

### Installation

```
pnpm dlx nuxi module add eslint
pnpm add -D @lttr/nuxt-config-eslint
```

### Example `eslint.config.js` file in a Nuxt app, which uses this package

```ts
// @ts-check
import withNuxt from "./.nuxt/eslint.config.mjs"
import customConfig from "@lttr/nuxt-config-eslint"

export default withNuxt(customConfig)
```

### Optional

```
pnpm dlx add-npm-scripts 'lint' 'eslint'
pnpm dlx add-npm-scripts 'lint:fix' 'eslint --fix'
pnpm dlx format-package --write
```
