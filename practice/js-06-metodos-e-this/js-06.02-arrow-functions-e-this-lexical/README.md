# JS-06.02 — Arrow Functions e `this` Lexical

Destacar como arrow functions tratam `this` diferente das funções tradicionais.

## Fundamentos

- **Arrow e `this`:** arrow não cria um novo `this`; ele herda (`fecha sobre`) o `this` do contexto léxico em que foi definido.
- **Imutabilidade de `this` em arrow:** nem `call/apply/bind` alteram o `this` em arrow (são ignoradas).
- **Uso comum:** arrow é útil para callbacks onde queremos usar `this` do escopo externo (por exemplo, em métodos de classe para callbacks de event).

## Competências

Ao concluir esta unidade, devo conseguir:

- Decidir quando usar arrow function para evitar rebinding de `this` (por exemplo, em closures de métodos).
- Explicar por que `this` permanece o mesmo (lexical) em arrow functions, ilustrando em código aninhado.
- Reconhecer que arrow não serve como construtora (`new` com arrow é erro).

## Prática

Os exercícios desta unidade aplicam os fundamentos estudados por meio de implementação, análise, diagnóstico e justificativa quando pertinentes.

[Ver exercícios →](./exercises/)

## Web Integration

Exemplificar em código de componente front-end (por exemplo, callback de evento ou método de objeto) usando função arrow para que `this` continue sendo o objeto desejado, evitando `undefined`.

[Ver Web Integration →](../../../web-integration/)

---

### Navegação

[← JS-06.01 — Chamada de Método e Contexto de `this`](../js-06.01-chamada-de-metodo-e-contexto-de-this/) ·
[↑ JS-06 — Métodos e `this`](../README.md) ·
[Checkpoint JS-06 →](../checkpoint/)
