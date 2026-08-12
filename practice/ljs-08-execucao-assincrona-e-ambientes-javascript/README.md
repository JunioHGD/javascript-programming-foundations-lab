# LJS-08 — Execução assíncrona e ambientes JavaScript

[JavaScript & Programming Foundations Lab](../../README.md) › [Prática](../README.md) › LJS-08

Este bloco estabelece o modelo fundamental de ambientes e execução assíncrona, distinguindo responsabilidades da linguagem e do host antes de trabalhar com Promises, `async`/`await` e filas de execução.

## Objetivo

Fornecer o modelo mínimo de assincronismo necessário para trabalhar posteriormente com browser e Node.js sem atribuir ao ECMAScript mecanismos pertencentes ao host.

## Unidades

### [LJS-08.01 — Linguagem, engine, runtime e host](./ljs-08.01-linguagem-engine-runtime-e-host/)

Estabelecer corretamente as responsabilidades das diferentes camadas.

### [LJS-08.02 — Promises](./ljs-08.02-promises/)

Representar e compor resultados que podem ficar disponíveis posteriormente.

### [LJS-08.03 — `async` e `await`](./ljs-08.03-async-e-await/)

Utilizar sintaxe assíncrona a partir do modelo já construído de Promises.

### [LJS-08.04 — Jobs, tasks e microtasks](./ljs-08.04-jobs-tasks-e-microtasks/)

Conhecer apenas a camada necessária para prever a ordem básica do código assíncrono.

## Checkpoint

O checkpoint consolida a distinção entre ECMAScript, engine, runtime e host e integra Promises, `async`/`await`, jobs, tasks e microtasks para prever a ordem básica da execução assíncrona.

[Ir para o checkpoint →](./checkpoint/)

---

[← LJS-07 — Módulos e falhas](../ljs-07-modulos-e-falhas/) · [↑ JavaScript & Programming Foundations Lab](../../README.md)
