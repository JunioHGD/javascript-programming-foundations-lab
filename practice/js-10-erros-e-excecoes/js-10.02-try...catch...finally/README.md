# JS-10.02 — `try...catch...finally`

Aprender a capturar e tratar exceções durante a execução de blocos de código.

## Fundamentos

- **Estrutura `try/catch`:** bloco `try` contém código “perigoso”; se ocorre `throw`, a execução pula para o `catch`. Se nenhum erro ocorre, `catch` é ignorado.
- **`finally`:** bloco opcional que é executado após `try`/`catch`, sempre (usado para limpeza).
- **Escopo de captura:** variáveis definidas em `catch (e)` só existem dentro do `catch`.
- **Re-throw:** em `catch` pode-se lançar novamente erro para propagar.

## Competências

Ao concluir esta unidade, devo conseguir:

- Envolver trechos de código suscetíveis a erro (como parse JSON ou operações que podem falhar) em `try/catch`.
- Extrair informações do objeto de erro capturado (`e.message`, `e.name`, `e.stack`) para log/diagnóstico.
- Decidir quando tratar o erro no local ou re-lançar para quem chamou.

## Prática

Os exercícios desta unidade aplicam os fundamentos estudados por meio de implementação, análise, diagnóstico e justificativa quando pertinentes.

[Ver exercícios →](./exercises/)

## Web Integration

Fazer `try { JSON.parse(input) } catch(e) { alert("JSON inválido") }` ao receber entrada do usuário, demonstrando tratamento de erros de parsing.

[Ver Web Integration →](../../../web-integration/)

---

### Navegação

[← JS-10.01 — `throw` e Objeto `Error`](../js-10.01-throw-e-objeto-error/) ·
[↑ JS-10 — Erros e Exceções](../README.md) ·
[Checkpoint JS-10 →](../checkpoint/)
