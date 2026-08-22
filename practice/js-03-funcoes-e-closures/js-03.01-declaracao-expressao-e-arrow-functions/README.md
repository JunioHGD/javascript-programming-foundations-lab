# JS-03.01 — Declaração, Expressão e Arrow Functions

Diferenciar as formas de criar funções em JavaScript e compreender que funções são valores.

## Fundamentos

- **Funções de primeira classe:** uma função pode ser atribuída, passada ou retornada como valor. Isso habilita callbacks e funções de ordem superior.
- **Declarações vs Expressões:** diferença entre `function nome() {}` (função nomeada) e `const nome = function(){}` ou arrow (`=>`) (função anônima atribuída).
- **Arrow functions:** sintaxe compacta; **não** cria novo escopo de `this` (captura o `this` léxico).
- **Parâmetros e retorno:** comportamento de parâmetros opcionais, valores default; retorno implícito em arrow de expressão única.

## Competências

Ao concluir esta unidade, devo conseguir:

- Escrever funções usando declaração e expressão (incluindo arrow) para o mesmo propósito, sabendo como as diferenças afetarão `this` e `arguments`.
- Passar funções como argumentos (callbacks) e receber funções de outras funções (higher-order).
- Converter uma função tradicional em arrow function onde aplicável, ou vice-versa, preservando funcionalidade.

## Prática

Os exercícios desta unidade aplicam os fundamentos estudados por meio de implementação, análise, diagnóstico e justificativa quando pertinentes.

[Ver exercícios →](./exercises/)

## Web Integration

Criar um manipulador de evento de clique passado como função de callback; observar como `this` (evento) é tratado dentro do handler quando escrito como função normal vs arrow.

[Ver Web Integration →](../../../web-integration/)

---

### Navegação

[↑ JS-03 — Funções e Closures](../README.md) ·
[JS-03.02 — Escopo Léxico e Closures →](../js-03.02-escopo-lexico-e-closures/)
