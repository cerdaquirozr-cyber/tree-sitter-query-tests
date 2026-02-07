# Pruebas de Consultas Tree-sitter

Conjunto de pruebas para validar **queries** en tree-sitter (JavaScript/TypeScript).

Pruebas sobre: construcción, matches, captures, predicados (#eq?, #match?, etc.), límites, timeouts, disableCapture/disablePattern.

## Estructura del repositorio
tree-sitter-query-tests/
├── tests/
│   └── query.test.ts       # Todas las pruebas (Vitest)
├── helper.ts               # Carga el lenguaje JavaScript
├── package.json
├── tsconfig.json
├── README.md
└── LICENSE                 # MIT


(src/ y vitest.config.ts no están por ahora, son opcionales)

## Requisitos

- Node.js ≥ 18
- npm

## Cómo correr las pruebas

```bash
git clone https://github.com/cerdaquiroz-cyber/Pruebas-de-consulta-de-tree-sitter.git
cd Pruebas-de-consulta-de-tree-sitter
npm install
npm test



(O usa npx vitest para modo watch)Si salen verdes → todo bien con tu tree-sitter.NotasUsa tree-sitter y tree-sitter-javascript ~0.25 o superior.

Si usas web-tree-sitter / WASM → descomenta opción 2 en helper.ts.

Sirve para detectar regresiones o validar forks.



LicenciaMIT License (./LICENSE) – libre para usar, modificar, compartir.Hecho por Ramón Cerda Quiroz (@RAMON_CERDA

) – 2026

¡Abre un issue si quieres mejorar algo!


**Pasos exactos para meterlo (desde el celular):**

1. Abre GitHub en el navegador del celular.
2. Entra a tu repo: https://github.com/cerdaquiroz-cyber/Pruebas-de-consulta-de-tree-sitter
3. Toca el archivo **README.md**
4. Toca el ícono de lápiz ✏️ (editar)
5. Borra TODO lo que hay ahí (selecciona todo y elimina)
6. Pega el texto de arriba (todo el bloque que empieza con # Pruebas...)
7. Abajo toca **Commit changes**
8. En el mensaje pon algo como: "README final limpio y claro"
9. Toca **Commit changes** otra vez.

Listo. En 1 minuto queda profesional y sin rollo.

Ya no repito más explicaciones largas. Si quieres cambiar algo (quitar una parte, poner más emojis, cambiar el título), dime qué línea cambiamos y te doy la versión nueva en 10 segundos.

¿Ya lo vas a pegar ahorita o quieres ajustar algo antes?  
(Es la 1:10 am, ve a dormir cuando termines carnal 😴)
