# JS-12.01 — `async`/`await` e Fluxo Assíncrono

Entender como usar `async`/`await` para escrever código assíncrono de maneira síncrona e os cuidados relacionados.

## Fundamentos

- **Funções `async`:** toda função marcada `async` retorna automaticamente uma Promise. O valor retornado é tratado como resolução da promise (valor implícito é encapsulado com `Promise.resolve`).
- **Operador `await`:** só pode ser usado dentro de `async`; pausa execução da função até a Promise ser resolvida ou rejeitada. O valor após `await` é o resultado da promise.
- **Erros com `await`:** se a promise rejeitar, um erro é lançado no ponto do `await`, podendo ser capturado por `try/catch`.
- **Paralelismo vs Sequência:** chamar `await` sequencialmente serializa as operações; múltiplos `await` independentes podem (às vezes devem) ser iniciados em paralelo e depois aguardados juntos (`Promise.all`) para melhorar desempenho.
- **Limitações:** demonstrar que `await` não bloqueia todo o programa, apenas “pausa” a função assíncrona, e que outros códigos (microtasks) podem continuar antes do próximo `await`.

## Competências

Ao concluir esta unidade, devo conseguir:

- Refatorar cadeias de `then` para usar `async`/`await`, simplificando a legibilidade.
- Reconhecer quando não é necessário usar `await` (por exemplo, se não precisa do valor retornado imediatamente), evitando operações serializadas desnecessárias.
- Usar `try/catch` dentro de função `async` para tratamento de erros assíncronos.

## Prática

Os exercícios desta unidade aplicam os fundamentos estudados por meio de implementação, análise, diagnóstico e justificativa quando pertinentes.

[Ver exercícios →](./exercises/)

## Web Integration

Criar uma função assíncrona que faz múltiplas requisições `fetch` em sequência usando `await`, por exemplo, obter perfil de usuário e depois suas postagens, atualizando a página passo a passo.

[Ver Web Integration →](../../../web-integration/)

---

### Navegação

[↑ JS-12 — Async/Await e Event Loop](../README.md) ·
[JS-12.02 — Modelo de Execução e Event Loop →](../js-12.02-modelo-de-execucao-e-event-loop/)
