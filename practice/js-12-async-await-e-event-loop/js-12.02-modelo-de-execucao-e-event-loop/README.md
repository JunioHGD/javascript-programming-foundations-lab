# JS-12.02 — Modelo de Execução e Event Loop

Explicar como o JavaScript executa código assíncrono sob a cobertura, focando em tasks, microtasks e ordenação de execução.

## Fundamentos

- **Call stack e jobs:** tarefas (jobs) são empilhadas na fila e executadas até conclusão (run-to-completion).
- **Tasks vs Microtasks:** eventos assíncronos e callbacks normais formam tasks (macrotasks), enquanto callbacks de Promises são microtasks. Microtasks são processadas antes de continuar no próximo tick de tasks.
- **Sem bloqueio:** o loop de eventos garante que I/O (timers, XHR, fetch) ocorrem assincronamente; o código após uma operação assíncrona só roda via callback ou promise (like `then`).
- **Exemplo de ordenação:** ilustrar que Promise.resolve().then(...) sempre roda antes de setTimeout(..., 0).

## Competências

Ao concluir esta unidade, devo conseguir:

- Descrever a ordem de execução entre código síncrono, `then` de promessa e callbacks de timers em um exemplo concreto.
- Prever resultados de código envolvendo múltiplos `setTimeout`, `Promise.then` e chamadas normais.
- Analisar brevemente porque `await` não interrompe eventos subsequentes pendentes: após `await`, o resto da função vira microtask.

## Prática

Os exercícios desta unidade aplicam os fundamentos estudados por meio de implementação, análise, diagnóstico e justificativa quando pertinentes.

[Ver exercícios →](./exercises/)

## Web Integration

Demonstrar em código front-end que atualizações via `setTimeout` e `Promise.then` ocorrem em ordem previsível: por exemplo, registrar no console a sequência de `console.log` no corpo principal, em um `.then()`, e em um `setTimeout`, verificando que `.then()` (microtask) executa antes do próximo tick de `setTimeout` (task).

[Ver Web Integration →](../../../web-integration/)

---

### Navegação

[← JS-12.01 — `async`/`await` e Fluxo Assíncrono](../js-12.01-async-await-e-fluxo-assincrono/) ·
[↑ JS-12 — Async/Await e Event Loop](../README.md) ·
[Checkpoint JS-12 →](../checkpoint/)
