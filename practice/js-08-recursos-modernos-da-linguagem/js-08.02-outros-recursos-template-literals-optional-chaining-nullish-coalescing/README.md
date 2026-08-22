# JS-08.02 — Outros Recursos: Template Literals, Optional Chaining, Nullish Coalescing

Conhecer sintaxes adicionais frequentes em código moderno.

## Fundamentos

- **Template literals:** strings delimitadas por acento grave, permitem interpolação `${...}` e multilinhas.
- **Optional chaining (`?.`):** acessar propriedades aninhadas sem erro se algum nível for `null`/`undefined`.
- **Nullish coalescing (`??`):** operar parecido com `||` mas somente consideram `null`/`undefined` como “vazios”.
- **Default parameters** (reforço): garantir valor padrão em parâmetros de função.

## Competências

Ao concluir esta unidade, devo conseguir:

- Construir strings complexas sem concatenação manual usando template literals.
- Proteger acessos a propriedades de objetos que podem ser nulos usando `?.`.
- Diferenciar `||` de `??` ao definir valores default (entender que `||` considera `0` e `""` como falsy, enquanto `??` não).

## Prática

Os exercícios desta unidade aplicam os fundamentos estudados por meio de implementação, análise, diagnóstico e justificativa quando pertinentes.

[Ver exercícios →](./exercises/)

## Web Integration

Criar strings de marcação HTML com template literals inserindo variáveis; acessar dados aninhados de objetos de resposta (por exemplo, `resp.data?.user?.name`) sem erro caso algo não exista.

[Ver Web Integration →](../../../web-integration/)

---

### Navegação

[← JS-08.01 — Destructuring, Spread e Rest](../js-08.01-destructuring-spread-e-rest/) ·
[↑ JS-08 — Recursos Modernos da Linguagem](../README.md) ·
[Checkpoint JS-08 →](../checkpoint/)
