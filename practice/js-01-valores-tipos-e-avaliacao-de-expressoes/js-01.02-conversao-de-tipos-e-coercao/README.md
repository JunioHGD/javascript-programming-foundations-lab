# JS-01.02 — Conversão de Tipos e Coerção

Entender como JS converte valores entre tipos em expressões e condições.

## Fundamentos

- **Coerção implícita:** concatenação string + número, comparação `==`.
- **Truthy/Falsy:** valores que avaliam como false em condicionais (false, `undefined`, `null`, `0`, `NaN`, `""`); todos os demais (incluindo objetos) são truthy.
- **Conversão explícita:** `Boolean()`, `String()`, `Number()`.
- **Igualdade:** diferenças entre `==` (com coerção) e `===` (sem coerção).
- **Comparações numéricas e de string:** comportamento de `<`, `>` com diferentes tipos.

## Competências

Ao concluir esta unidade, devo conseguir:

- Avaliar expressões que envolvem conversão de tipo (por exemplo, `'5' + 2` ou `5 == '5'`).
- Prever resultados de condicionais sabendo quais valores são truthy ou falsy.
- Justificar por que `null == undefined` é true, mas `null === undefined` é false.

## Prática

Os exercícios desta unidade aplicam os fundamentos estudados por meio de implementação, análise, diagnóstico e justificativa quando pertinentes.

[Ver exercícios →](./exercises/)

## Web Integration

Implementar validação simples: por exemplo, ler um input numérico como texto e converter para número com `Number()`; verificar se a conversão falhou (`NaN`) antes de usar o valor.

[Ver Web Integration →](../../../web-integration/)

---

### Navegação

[← JS-01.01 — Tipos Primitivos e Objetos](../js-01.01-tipos-primitivos-e-objetos/) ·
[↑ JS-01 — Valores, Tipos e Avaliação de Expressões](../README.md) ·
[Checkpoint JS-01 →](../checkpoint/)
