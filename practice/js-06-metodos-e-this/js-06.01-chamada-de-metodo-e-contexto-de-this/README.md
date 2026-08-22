# JS-06.01 — Chamada de Método e Contexto de `this`

Entender como o modo de chamar uma função define o valor de `this`.

## Fundamentos

- **Chamada de método:** `obj.metodo()` vincula `this` a `obj`. Mesmo se `metodo` vier de um protótipo, o contexto é o objeto que fez a chamada.
- **Função solta:** chamar `func()` isoladamente (sem objeto) define `this` como `undefined` (modo estrito) ou `globalThis` (modo não estrito).
- **Call, apply, bind:** métodos para chamar explicitamente `this` em uma função.
- **Perda de contexto:** passar método de objeto como callback pode “perder” o `this` original (muda para indefinido/global se não for restrito).

## Competências

Ao concluir esta unidade, devo conseguir:

- Prever o valor de `this` em diferentes formas de invocação: `obj.metodo()`, `metodo()` descarregado, ou `metodo.call(outro)`.
- Resolver cenários comuns de perda de `this` (por exemplo, armazenar `const f = obj.metodo; f()`; ou usar em callback de evento DOM).
- Usar `bind` ou closures para preservar o contexto adequado quando necessário.

## Prática

Os exercícios desta unidade aplicam os fundamentos estudados por meio de implementação, análise, diagnóstico e justificativa quando pertinentes.

[Ver exercícios →](./exercises/)

## Web Integration

Criar um botão `<button>` cujo manipulador chama um método de um objeto; mostrar que, sem bind, o `this` dentro do método é o elemento do DOM, e com arrow/bind pode ser o objeto desejado.

[Ver Web Integration →](../../../web-integration/)

---

### Navegação

[↑ JS-06 — Métodos e `this`](../README.md) ·
[JS-06.02 — Arrow Functions e `this` Lexical →](../js-06.02-arrow-functions-e-this-lexical/)
