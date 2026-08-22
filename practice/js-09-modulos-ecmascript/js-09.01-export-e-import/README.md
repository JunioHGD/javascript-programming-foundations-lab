# JS-09.01 — `export` e `import`

Compreender a sintaxe básica de exportação e importação de valores entre módulos.

## Fundamentos

- **Exportações nomeadas e default:** `export {val1, val2}` vs `export default`, e `import {val1} from` vs `import valDefault from`.
- **Bindings estáticos:** importações criam referências vivas aos valores exportados (read-only local).
- **Escopo de módulo:** cada arquivo é executado em seu próprio escopo; não polui global.
- **Carregamento em browsers:** uso de `<script type="module">` e caminhos relativos para arquivos JS.

## Competências

Ao concluir esta unidade, devo conseguir:

- Configurar dois arquivos JS onde um exporta funções/valores e outro importa usando `import`.
- Escolher entre export default ou nomeados dependendo do caso de uso (objeto utilitário vs módulo single feature).
- Prever erros comuns: esquecer `export`, usar nome errado em import, ou não incluir `.js` no caminho.

## Prática

Os exercícios desta unidade aplicam os fundamentos estudados por meio de implementação, análise, diagnóstico e justificativa quando pertinentes.

[Ver exercícios →](./exercises/)

## Web Integration

Criar um módulo `utils.js` que exporta funções de formatação de data e importar em `main.js` para formatar uma data na página.

[Ver Web Integration →](../../../web-integration/)

---

### Navegação

[↑ JS-09 — Módulos ECMAScript](../README.md) ·
[JS-09.02 — Módulos em Prática →](../js-09.02-modulos-em-pratica/)
