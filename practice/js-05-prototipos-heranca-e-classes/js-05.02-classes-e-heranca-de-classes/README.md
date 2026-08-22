# JS-05.02 — Classes e Herança de Classes

Entender a sintaxe `class` e sua relação com o modelo de protótipos.

## Fundamentos

- **Sintaxe `class`:** declaração de classe com `constructor`, métodos, `extends`, `super`.
- **Instâncias:** uso de `new` para criar objetos cuja `[[Prototype]]` é a função `constructor.prototype`.
- **Herança de classes:** `class Sub extends Base` faz `Sub.prototype.[[Prototype]] = Base.prototype`.
- **Classes são açúcar sintático:** internamente equivalem a função construtora + protótipo; métodos definidos na classe são não-enumeráveis.

## Competências

Ao concluir esta unidade, devo conseguir:

- Definir uma classe JS com construtor e métodos; criar instâncias e acessar métodos herdados.
- Desenhar uma hierarquia simples de classes (`extends`) e explicar como o protótipo é encadeado.
- Comparar código equivalente entre sintaxe de classe e funções construtoras + protótipo, reconhecendo semântica igual.

## Prática

Os exercícios desta unidade aplicam os fundamentos estudados por meio de implementação, análise, diagnóstico e justificativa quando pertinentes.

[Ver exercícios →](./exercises/)

## Web Integration

Modelar entidades de uma aplicação web com classes: por exemplo, criar classes `Card`, `Deck` ou `Usuario` para gerenciar dados do front-end e instanciar objetos.

[Ver Web Integration →](../../../web-integration/)

---

### Navegação

[← JS-05.01 — Cadeia de Protótipos](../js-05.01-cadeia-de-prototipos/) ·
[↑ JS-05 — Protótipos, Herança e Classes](../README.md) ·
[Checkpoint JS-05 →](../checkpoint/)
