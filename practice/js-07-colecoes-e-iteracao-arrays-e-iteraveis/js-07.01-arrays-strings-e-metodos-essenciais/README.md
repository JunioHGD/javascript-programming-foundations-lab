# JS-07.01 — Arrays, Strings e Métodos Essenciais

Entender arrays (e imutabilidade relativa de strings) como coleções, e usar métodos comuns de transformação.

## Fundamentos

- **Arrays:** são objetos indexados (chaves numéricas); possuem propriedade `length` dinâmica. Atribuir a índices (mesmo além do atual `length`) ajusta automaticamente o tamanho.
- **Strings:** sequências imutáveis de caracteres. Indexação produz caracteres e permite iteração. Possuem métodos próprios (slice, toUpperCase, etc.).
- **Métodos de array:** mutadores (`push`, `pop`, `splice`, etc.) versus não-mutadores (`map`, `filter`, `slice`). Usar `map/filter` para processamento declarativo e evitar mudança de estado global.
- **Spread e rest para coleções:** espalhar (`...array`) para copiar ou concatenar; coletar em parâmetros (`...args`). Desestruturação básica de arrays e strings.

## Competências

Ao concluir esta unidade, devo conseguir:

- Prever o resultado de operações de array, incluindo métodos mutáveis vs não-mutáveis.
- Reescrever loops tradicionais usando métodos de array (`map`, `filter`) quando adequado.
- Aplicar desestruturação de array e spread para clonar ou extrair partes de arrays/strings.

## Prática

Os exercícios desta unidade aplicam os fundamentos estudados por meio de implementação, análise, diagnóstico e justificativa quando pertinentes.

[Ver exercícios →](./exercises/)

## Web Integration

Consumir uma lista de dados (p.ex. itens de um JSON) usando `fetch` em uma função assíncrona e preencher elementos `<li>` via `map`; ou usar `filter` para destacar itens que cumprem certo critério na página.

[Ver Web Integration →](../../../web-integration/)

---

### Navegação

[↑ JS-07 — Coleções e Iteração (Arrays e Iteráveis)](../README.md) ·
[JS-07.02 — Iteração e Iteráveis →](../js-07.02-iteracao-e-iteraveis/)
