# JS-11.01 — Callbacks e Fluxo Assíncrono

Entender o padrão antigo de callbacks para operações assíncronas.

## Fundamentos

- **Callbacks:** passar função para ser executada ao fim de operação assíncrona (por exemplo, `setTimeout(fn, ms)` ou um pedido AJAX).
- **Problemas de callback:** múltiplos callbacks aninhados (“callback hell”) dificultam leitura e tratamento de erros.
- **Sequenciamento assíncrono:** como evitar condições de corrida garantindo que callbacks sejam chamados na ordem desejada.

## Competências

Ao concluir esta unidade, devo conseguir:

- Registrar múltiplos callbacks e prever a ordem de execução baseada nos tempos/delays.
- Transformar código com callbacks aninhados em uma sequência linear usando técnicas como funções encadeadas.
- Identificar onde callbacks podem falhar silenciosamente e a importância de funções de erro (ex. callback(err, data)).

## Prática

Os exercícios desta unidade aplicam os fundamentos estudados por meio de implementação, análise, diagnóstico e justificativa quando pertinentes.

[Ver exercícios →](./exercises/)

## Web Integration

Configurar `setTimeout` ou `setInterval` para atualizar elementos DOM após atrasos, provando que o resto do script continua executando sem bloqueio.

[Ver Web Integration →](../../../web-integration/)

---

### Navegação

[↑ JS-11 — Assíncronismo e Promises](../README.md) ·
[JS-11.02 — Promises: Estado e Encadeamento →](../js-11.02-promises-estado-e-encadeamento/)
