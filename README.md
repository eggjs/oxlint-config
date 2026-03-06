# @eggjs/oxlint-config

Shared [oxlint](https://oxc.rs/docs/guide/usage/linter) config for eggjs projects.

## Install

```bash
npm i @eggjs/oxlint-config --save-dev
```

## Usage

### With vite-plus (`vite.config.ts`)

```ts
import { defineConfig } from 'vite-plus';
import oxlintConfig from '@eggjs/oxlint-config';

export default defineConfig({
  lint: {
    extends: [oxlintConfig],
    // your overrides...
  },
});
```

### With `oxlint.config.mjs`

```js
import { defineConfig } from 'oxlint';
import eggConfig from '@eggjs/oxlint-config';

export default defineConfig({
  extends: [eggConfig],
  // your overrides...
});
```

### Legacy JSON config (v1)

The `.oxlintrc.json` file is still available for direct use:

```bash
oxlint -c node_modules/@eggjs/oxlint-config/.oxlintrc.json
```

## License

[MIT](LICENSE)
