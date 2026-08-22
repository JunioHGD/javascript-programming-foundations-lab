# JS-11.02 — Promises: Estado e Encadeamento

Aprender o uso de Promises para representar operações assíncronas de forma encadeável e estruturada.

## Fundamentos

- **Criação de Promise:** `new Promise((resolve, reject) => {...})`.
- **Estados da Promise:** `pending`, `fulfilled` (resolvida com valor), `rejected` (erro).
- **`then`, `catch`, `finally`:** encadeamento de tratamento: `then(onFulfilled, onRejected)` adiciona callbacks que serão chamados quando a promise resolver; `catch` é atalhos para tratar erros; `finally` executa independente do resultado.
- **Encadeamento:** `then()` retorna uma nova promise permitindo sequenciar ações. Erros não tratados sobem até o próximo `catch`.
- **Evitar callback hell:** comparar estrutura de encadeamento de promises (flat) com aninhamento de callbacks.

## Competências

Ao concluir esta unidade, devo conseguir:

- Converter código assíncrono baseado em callback para usar Promises (`resolve` e `reject`).
- Encadear várias operações assíncronas: usar `then` sequencialmente para processar resultados intermediários, assegurando fluxo correto.
- Lidar com erros em cadeia: observar como lançar/exceção dentro de `then` pula para o próximo `catch`.
- Conhecer métodos estáticos úteis (`Promise.all`, `Promise.resolve`, etc.) em nível básico.

## Prática

Os exercícios desta unidade aplicam os fundamentos estudados por meio de implementação, análise, diagnóstico e justificativa quando pertinentes.

[Ver exercícios →](./exercises/)

## Web Integration

Fazer uma requisição com a API `fetch` (retorna Promise) para trazer dados de uma API pública e então encadear `.then()` para processar JSON e atualizar a página. Demonstrar `catch` para erro de rede.

[Ver Web Integration →](../../../web-integration/)

---

### Navegação

[← JS-11.01 — Callbacks e Fluxo Assíncrono](../js-11.01-callbacks-e-fluxo-assincrono/) ·
[↑ JS-11 — Assíncronismo e Promises](../README.md) ·
[Checkpoint JS-11 →](../checkpoint/)
