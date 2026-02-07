# tree-sitter-query-tests/
├── src/                    ← si después agregas código fuente (por ahora vacío o con el helper)
├── tests/
│   └── query.test.ts       ← el archivo grande que me pasaste
├── helper.ts               ← el helper que te di antes (ajustado)
├── package.json
├── tsconfig.json           ← importante para TypeScript + vitest
├── vitest.config.ts        ← opcional pero recomendado
├── README.md
└── LICENSE
// helper.ts
import type { Language } from 'tree-sitter';

let cachedJavaScript: Language | undefined;

export default {
  async get JavaScript(): Promise<Language> {
    if (cachedJavaScript) return cachedJavaScript;

    // Opción 1: tree-sitter oficial (recomendado para empezar)
    const JavaScript = (await import('tree-sitter-javascript')).default;

    // Opción 2: si usas web-tree-sitter o wasm
    // const { Language } = await import('web-tree-sitter');
    // const JavaScript = await Language.load('/node_modules/tree-sitter-javascript/tree-sitter-javascript.wasm');

    cachedJavaScript = JavaScript as Language;
    return cachedJavaScript;
  }
};# bash-ts-json-package

Conjunto de pruebas (test suite) para validar el comportamiento de las **Queries** en tree-sitter (bindings de JavaScript/TypeScript).

Basado en pruebas exhaustivas de construcción, matches, captures, predicados, límites, timeouts, etc.

## Instalación

```bash
git clone https://github.com/RAMON_CERDA/bash-ts-json-package.git
cd bash-ts-json-package
npm install
