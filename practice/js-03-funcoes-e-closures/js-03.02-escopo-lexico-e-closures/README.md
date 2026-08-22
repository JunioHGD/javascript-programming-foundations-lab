# JS-03.02 — Escopo Léxico e Closures

Compreender o escopo léxico de funções e como closures preservam variáveis do contexto de criação.

## Fundamentos

- **Escopo léxico:** cada função “fecha sobre” o ambiente em que foi definida.
- **Closure:** quando uma função interna referencia variáveis do escopo externo, essas variáveis permanecem acessíveis mesmo após o término da execução externa.
- **Estado privado:** uso de closures para manter estado entre chamadas (padrões como contador), sem expor variáveis globalmente.
- **Lifetime dos bindings:** variáveis em closures só são coletadas se não houver mais referência à função ou ao próprio binding.

## Competências

Ao concluir esta unidade, devo conseguir:

- Prever quais variáveis cada função aninhada pode acessar, dado um exemplo de múltiplos níveis de função.
- Usar closures para implementar padrões (por exemplo, função que retorna outra função que incrementa um contador interno).
- Identificar e corrigir bugs comuns de closure, como o “capturar laço com var” (falha em closures dentro de loops usando `var`).

## Prática

Os exercícios desta unidade aplicam os fundamentos estudados por meio de implementação, análise, diagnóstico e justificativa quando pertinentes.

[Ver exercícios →](./exercises/)

## Web Integration

Implementar um contador clicável que mantém o número de cliques em um closure (por exemplo, `let count=0; return () => {count++; ...}`), demonstrando persistência de estado privado.

[Ver Web Integration →](../../../web-integration/)

---

### Navegação

[← JS-03.01 — Declaração, Expressão e Arrow Functions](../js-03.01-declaracao-expressao-e-arrow-functions/) ·
[↑ JS-03 — Funções e Closures](../README.md) ·
[Checkpoint JS-03 →](../checkpoint/)
