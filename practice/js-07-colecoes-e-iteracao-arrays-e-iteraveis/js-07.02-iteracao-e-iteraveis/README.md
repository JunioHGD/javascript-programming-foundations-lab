# JS-07.02 — Iteração e Iteráveis

Aprender a iterar de forma geral sobre estruturas de coleção e outros iteráveis.

## Fundamentos

- **Loops tradicionais:** `for`, `while`, mas enfatizar `for...of` para arrays e iteráveis (objetos que implementam `@@iterator`).
- **for...in vs for...of:** para objetos genéricos, `for-in` itera chaves enumeráveis, mas para arrays recomenda-se `for-of`.
- **Iteradores e geradores:** menção ao protocolo de iteração (`Symbol.iterator`) e iteráveis padrão (`Array`, `String`, `Map`, `Set`, etc.).
- **Atenção a mutações durante iteração:** explicar como modificar array dentro do loop pode afetar resultados.

## Competências

Ao concluir esta unidade, devo conseguir:

- Escolher o laço adequado a cada situação: percorrer índices, percorrer valores ou chaves de objeto.
- Usar `for...of` com arrays e strings, entender que percorre valores (iteração sequencial).
- Iterar sobre objetos (via `Object.keys` ou `for...in`) corretamente.

## Prática

Os exercícios desta unidade aplicam os fundamentos estudados por meio de implementação, análise, diagnóstico e justificativa quando pertinentes.

[Ver exercícios →](./exercises/)

## Web Integration

Por exemplo, iterar sobre um `HTMLCollection` ou `NodeList` (que são iteráveis) usando `for...of`, para atribuir event listeners a múltiplos elementos de forma simples.

[Ver Web Integration →](../../../web-integration/)

---

### Navegação

[← JS-07.01 — Arrays, Strings e Métodos Essenciais](../js-07.01-arrays-strings-e-metodos-essenciais/) ·
[↑ JS-07 — Coleções e Iteração (Arrays e Iteráveis)](../README.md) ·
[Checkpoint JS-07 →](../checkpoint/)
