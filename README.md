# Eslint config for Nuxt

An opinionated Eslint config for Nuxt apps.

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
import { wrapNuxtEslintConfig } from "@lttr/nuxt-config-eslint"

export default wrapNuxtEslintConfig(withNuxt())
```

### Optional

```
echo "dist" >> .eslintignore
pnpm dlx add-npm-scripts 'lint' 'eslint'
pnpm dlx add-npm-scripts 'lint:fix' 'eslint --fix'
pnpm dlx format-package --write
```
