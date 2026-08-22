# JS-02.01 — Declarações `var`, `let` e `const`

Conhecer diferenças fundamentais entre `var`, `let` e `const`, incluindo escopo e hoisting.

## Fundamentos

- **Hoisting de `var`:** declarações de `var` são içadas ao topo da função (ou global) e inicializadas com `undefined`.
- **Escopo de bloco (`let`/`const`):** variáveis declaradas com `let` ou `const` só existem no bloco `{}` em que são definidas.
- **TDZ (Temporal Dead Zone):** `let` e `const` só são inicializadas no momento da declaração; acessar antes causa erro de referência.
- **Reatribuição:** `const` cria bindings imutáveis (identificador constante), diferentemente de `let`.

## Competências

Ao concluir esta unidade, devo conseguir:

- Prever o valor de variáveis declaradas com `var` quando usadas antes da declaração (resultando em `undefined`).
- Identificar erros de referência quando um `let`/`const` é acessado antes de definido.
- Reescrever código para evitar vazamento acidental de variáveis globais (por exemplo, mudando `var` para `let`).

## Prática

Os exercícios desta unidade aplicam os fundamentos estudados por meio de implementação, análise, diagnóstico e justificativa quando pertinentes.

[Ver exercícios →](./exercises/)

## Web Integration

Implementar um contador simples usando `let` dentro de um evento de clique; demonstrar que a variável não existe fora da função (evitando poluir escopo global).

[Ver Web Integration →](../../../web-integration/)

---

### Navegação

[↑ JS-02 — Bindings, Declarações e Escopo Léxico](../README.md) ·
[JS-02.02 — Escopo Léxico e Shadowing →](../js-02.02-escopo-lexico-e-shadowing/)
