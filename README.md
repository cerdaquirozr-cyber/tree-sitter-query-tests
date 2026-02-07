# Pruebas de Consultas Tree-sitter (tree-sitter-query-tests)

Conjunto de pruebas unitarias (test suite) para validar el comportamiento de las **Queries** en **tree-sitter** (bindings de JavaScript/TypeScript).

Incluye pruebas exhaustivas sobre:
- Construcción de queries (errores de sintaxis y predicados)
- `.matches()` y búsqueda en rangos
- `.captures()` con orden correcto y predicados (#eq?, #match?, #not-match?, #any-eq?, etc.)
- Comparación entre capturas, propiedades (#set!, #is?)
- Límites de matches, timeouts y progress callback
- Deshabilitar capturas/patrones y cuantificadores

Ideal para validar forks, bindings personalizados o versiones de tree-sitter.

## Estructura del proyecto
