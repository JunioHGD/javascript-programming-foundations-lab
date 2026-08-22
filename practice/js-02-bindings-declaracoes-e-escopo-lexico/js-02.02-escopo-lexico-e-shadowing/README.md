# JS-02.02 — Escopo Léxico e Shadowing

Explicar como as funções criam novos escopos e como a resolução de nomes ocorre (lookup léxico).

## Fundamentos

- **Escopo de função:** cada função (declarada ou expressa) cria um novo ambiente léxico para seus parâmetros/variáveis.
- **Escopo global:** declarações fora de funções definem bindings globais (no `globalThis`).
- **Shadowing:** variáveis internas podem ocultar (shadow) variáveis externas com mesmo nome.
- **Ambientes léxicos:** modelo de cadeia de contextos onde cada referência é resolvida no escopo atual ou, se não existir, nos escopos superiores até o global.

## Competências

Ao concluir esta unidade, devo conseguir:

- Determinar qual valor uma referência de variável acessa, em presença de variáveis com mesmo nome em escopos aninhados.
- Explicar por que determinada variável é ou não visível em cada parte do código.
- Reorganizar código para evitar conflitos de nome e dependências implícitas de escopo.

## Prática

Os exercícios desta unidade aplicam os fundamentos estudados por meio de implementação, análise, diagnóstico e justificativa quando pertinentes.

[Ver exercícios →](./exercises/)

## Web Integration

Exibir dinamicamente múltiplas mensagens distintas usando variáveis de mesmo nome em diferentes funções de eventos (por exemplo, nome do usuário em formulário vs em função de limpeza).

[Ver Web Integration →](../../../web-integration/)

---

### Navegação

[← JS-02.01 — Declarações `var`, `let` e `const`](../js-02.01-declaracoes-var-let-e-const/) ·
[↑ JS-02 — Bindings, Declarações e Escopo Léxico](../README.md) ·
[Checkpoint JS-02 →](../checkpoint/)
