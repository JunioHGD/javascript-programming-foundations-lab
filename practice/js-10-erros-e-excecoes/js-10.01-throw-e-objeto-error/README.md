# JS-10.01 — `throw` e Objeto `Error`

Aprender a gerar erros propositais e usar objetos de erro padrão.

## Fundamentos

- **Instrução `throw`:** lança uma exceção imediatamente, interrompendo o fluxo atual; qualquer expressão pode ser lançada.
- **Objetos `Error`:** criação de novos erros personalizados (`new Error("mensagem")` ou subtipos como `TypeError`). Diferenciação entre lançar string vs objeto (boa prática usar objetos).
- **Propagação de erro:** exceções não tratadas sobem a pilha até o próximo `catch` ou terminam o programa.

## Competências

Ao concluir esta unidade, devo conseguir:

- Usar `throw new Error("msg")` para validar argumentos de função e sinalizar condições inválidas.
- Criar erros específicos (por exemplo, `throw new RangeError()` para índices fora de faixa).
- Entender que, em funções assíncronas (promises, callbacks), `throw` rejeita a promise automaticamente.

## Prática

Os exercícios desta unidade aplicam os fundamentos estudados por meio de implementação, análise, diagnóstico e justificativa quando pertinentes.

[Ver exercícios →](./exercises/)

## Web Integration

No contexto de formulário, validar dados e lançar um erro com `throw` quando o usuário envia informação inválida (por exemplo, formato de email), então capturar esse erro para exibir uma mensagem ao usuário.

[Ver Web Integration →](../../../web-integration/)

---

### Navegação

[↑ JS-10 — Erros e Exceções](../README.md) ·
[JS-10.02 — `try...catch...finally` →](../js-10.02-try...catch...finally/)
