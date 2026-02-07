# Pruebas de Consultas Tree-sitter

Conjunto de pruebas para validar **queries** en tree-sitter (JavaScript/TypeScript).

Pruebas sobre: construcción, matches, captures, predicados (#eq?, #match?, etc.), límites, timeouts, disableCapture/disablePattern.

## Estructura del repositorio
it('returns an array of child nodes', () => {
  tree = parser.parse('x10 + 1000')!;
  const sumNode = tree.rootNode.firstChild!.firstChild!;
  expect(sumNode.children.map(child => child.type)).toEqual(['identifier', '+', 'number']);
});
