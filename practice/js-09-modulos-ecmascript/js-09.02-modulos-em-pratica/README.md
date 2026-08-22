# JS-09.02 — Módulos em Prática

Entender carregamento e avaliação de módulos em cenário real.

## Fundamentos

- **Módulos vs scripts clássicos:** módulos são “deferidos” por padrão, têm escopo próprio e são avaliados uma vez.
- **Import maps (opcional):** breve menção de como especificar caminhos personalizados em browsers modernos.
- **Dependências cíclicas:** noções básicas do que pode dar errado se dois módulos se importam mutuamente (posições de execução).
- **Modularização:** benefícios de encapsular código em módulos, evitando variáveis globais e facilitando manutenção.

## Competências

Ao concluir esta unidade, devo conseguir:

- Integrar módulos em um HTML real usando `<script type="module">`.
- Diagnosticar problemas de importação em aplicações de múltiplos arquivos (ex: ordem de carregamento, erros de console sobre módulos).
- Explicar por que módulos permitem compartilhar código sem `window.` e como a reutilização é facilitada.

## Prática

Os exercícios desta unidade aplicam os fundamentos estudados por meio de implementação, análise, diagnóstico e justificativa quando pertinentes.

[Ver exercícios →](./exercises/)

## Web Integration

Construir página HTML que importa módulos JS: por exemplo, `index.html` carrega `app.js` que por sua vez importa funções de `domUtils.js` e `data.js` para montar conteúdo da página.

[Ver Web Integration →](../../../web-integration/)

---

### Navegação

[← JS-09.01 — `export` e `import`](../js-09.01-export-e-import/) ·
[↑ JS-09 — Módulos ECMAScript](../README.md) ·
[Checkpoint JS-09 →](../checkpoint/)
