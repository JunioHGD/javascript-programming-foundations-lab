# JS-04.02 — Identidade, Referência e Mutabilidade

Entender que objetos são armazenados por referência, como compartilhar e copiar seu conteúdo.

## Fundamentos

- **Identidade de objeto:** cada objeto tem identidade única; atribuir a outra variável cria outra referência para o mesmo objeto.
- **Comparação:** comparação de objetos com `==`/`===` só verifica identidade (mesmo objeto), não estrutura.
- **Mutabilidade:** alterar um objeto afeta todas as referências.
- **Cópias rasas:** duplicar objeto/array superficialmente (`Object.assign`, spread `{...obj}`), sabendo que isso copia referências internas.
- **Cópias profundas:** nota sobre necessidade (não embutida em JS, requer manual ou API).
- **Objetos aninhados:** atenção especial, pois referências internas também podem ser compartilhadas.

## Competências

Ao concluir esta unidade, devo conseguir:

- Prever efeitos de aliasing: dado código onde múltiplas variáveis referenciam o mesmo objeto, apontar como uma mudança será vista em todas.
- Implementar cópia rasa de objeto/array; explicar por que propriedades aninhadas ainda ficam compartilhadas.
- Identificar bugs de mutação involuntária (por exemplo, array copiado por atribuição e modificado em outro escopo).

## Prática

Os exercícios desta unidade aplicam os fundamentos estudados por meio de implementação, análise, diagnóstico e justificativa quando pertinentes.

[Ver exercícios →](./exercises/)

## Web Integration

Manusear uma lista de itens em um objeto (ou array) compartilhado entre funções de callback (e.g. adicionar/remover itens num carrinho de compras), observando efeitos de referência.

[Ver Web Integration →](../../../web-integration/)

---

### Navegação

[← JS-04.01 — Criação e Acesso a Propriedades](../js-04.01-criacao-e-acesso-a-propriedades/) ·
[↑ JS-04 — Objetos: Propriedades, Referências e Mutabilidade](../README.md) ·
[Checkpoint JS-04 →](../checkpoint/)
