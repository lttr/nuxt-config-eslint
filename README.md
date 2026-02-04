# Eslint config for Nuxt

An opinionated Eslint config for Nuxt apps.

## What's included

This config is designed to extend `@nuxt/eslint` module which already provides:

- `vue/essential` - error prevention rules
- `vue/strongly-recommended` - readability rules
- `vue/recommended` - community conventions

This package adds opinionated rules on top:

- `vue/block-lang` - enforce TypeScript in script blocks
- `vue/block-order` - enforce template/script/style order
- `vue/component-api-style` - enforce `<script setup>`
- `vue/define-props-declaration` - enforce type-based props
- `vue/v-for-delimiter-style` - enforce `of` over `in`
- `vue/component-name-in-template-casing` - PascalCase components
- `vue/require-typed-ref` - typed ref() calls
- `vue-scoped-css/recommended` - scoped CSS best practices
- `vuejs-accessibility/recommended` - a11y rules

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
