# JS-05.01 — Cadeia de Protótipos

Compreender como objetos podem herdar propriedades via protótipos.

## Fundamentos

- **Prototype chain:** todo objeto criado (literal, array, função) tem um link `[[Prototype]]` para outro objeto padrão (e.g., `Array.prototype`, `Object.prototype`).
- **Lookup de propriedade:** ao acessar `obj.prop`, JS procura primeiro em `obj`; se não encontrar, vai para `obj.[[Prototype]]` e assim por diante até null.
- **Alterando protótipos:** uso de `Object.create`, `__proto__`, ou definindo propriedades em `Constructor.prototype` para afetar instâncias futuras.
- **Herança de comportamento:** dar exemplos onde métodos nativos (como `toString`) vem de `Object.prototype`.

## Competências

Ao concluir esta unidade, devo conseguir:

- Rastrear onde uma propriedade/método é encontrado em um objeto ou em sua cadeia (detalhar a sequência de busca).
- Escolher entre definir método diretamente no objeto ou no protótipo, justificando impacto na herança.
- Evitar armadilhas de herança, por exemplo, entender que alterar um protótipo afeta todas as instâncias.

## Prática

Os exercícios desta unidade aplicam os fundamentos estudados por meio de implementação, análise, diagnóstico e justificativa quando pertinentes.

[Ver exercícios →](./exercises/)

## Web Integration

Criar uma cadeia prototípica customizada: por exemplo, definir `Animal` como função construtora e adicionar método a `Animal.prototype`, instanciar e usar método herdado em instâncias (animais diferentes).

[Ver Web Integration →](../../../web-integration/)

---

### Navegação

[↑ JS-05 — Protótipos, Herança e Classes](../README.md) ·
[JS-05.02 — Classes e Herança de Classes →](../js-05.02-classes-e-heranca-de-classes/)
