# Eslint config for Nuxt

An opinionated Eslint config for Nuxt apps.

## Usage

### Example `eslint.config.js` file in a Nuxt app, which uses this package

```ts
import withNuxt from "./.nuxt/eslint.config.mjs"
import { wrapNuxtEslintConfig } from "@lttr/nuxt-config-eslint"

export default wrapNuxtEslintConfig(withNuxt())
```
