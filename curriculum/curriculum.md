# JavaScript Foundations Lab — Currículo Canônico

## Escopo

O **JavaScript Foundations Lab** forma desenvolvedores capazes de **entender profundamente a linguagem JavaScript (ECMAScript)** e seus mecanismos essenciais, preparando-se tanto para front-end quanto back-end. Ele foca no *core* da linguagem e em como JavaScript executa conceitos de programação (valores, funções, escopo, objetos, módulos, erros, assincronismo) segundo seu próprio modelo, **não** revisando lógica de programação genérica (já coberta em outro Lab) nem se estendendo detalhadamente a APIs de ambiente. Em resumo, este Lab ensina **como JavaScript funciona por baixo do capô**, enquanto a familiaridade com DOM/Web APIs e recursos específicos de Node fica fora do núcleo (embora seus conhecimentos mínimos sejam usados em atividades de Web Integration).

Para evitar ambiguidades: *ECMAScript* (o padrão) define a sintaxe, tipos e comportamentos da linguagem, mas **JavaScript** no contexto web inclui também APIs do navegador (DOM, *fetch*, timers etc.). Este currículo diferencia claramente linguagem e ambiente. Por exemplo, `Array`, `Promise` e `JSON` são parte da biblioteca padrão ECMAScript, enquanto o DOM ou as APIs de arquivos só existem nos ambientes host (navegador ou Node).

Em relação ao *Programming Logic Foundations Lab*, este Lab **não repete** conceitos como “o que é uma condição ou laço” em termos gerais. Em vez disso, mostra **como JS interpreta e executa** essas construções: por exemplo, em vez de “o que é uma condição”, aborda como JavaScript converte e julga valores em contextos booleanos (truthy/falsy); em vez de “o que é uma função”, aprofunda como funções são objetos de primeira classe, criadas e chamadas no modelo JS, incluindo escopo e closures; em vez de “o que é um registro/struct”, investiga como objetos JavaScript representam dados, identidade e comportamento. Em suma, este Lab forma o desenvolvedor capaz de **prever o comportamento de código JS profissional**, não apenas memorizar sintaxe.

## Mapa curricular

| ID | Bloco |
|:---:|---|
| `JS-01` | [Valores, Tipos e Avaliação de Expressões](../practice/js-01-valores-tipos-e-avaliacao-de-expressoes/) |
| `JS-02` | [Bindings, Declarações e Escopo Léxico](../practice/js-02-bindings-declaracoes-e-escopo-lexico/) |
| `JS-03` | [Funções e Closures](../practice/js-03-funcoes-e-closures/) |
| `JS-04` | [Objetos: Propriedades, Referências e Mutabilidade](../practice/js-04-objetos-propriedades-referencias-e-mutabilidade/) |
| `JS-05` | [Protótipos, Herança e Classes](../practice/js-05-prototipos-heranca-e-classes/) |
| `JS-06` | [Métodos e `this`](../practice/js-06-metodos-e-this/) |
| `JS-07` | [Coleções e Iteração (Arrays e Iteráveis)](../practice/js-07-colecoes-e-iteracao-arrays-e-iteraveis/) |
| `JS-08` | [Recursos Modernos da Linguagem](../practice/js-08-recursos-modernos-da-linguagem/) |
| `JS-09` | [Módulos ECMAScript](../practice/js-09-modulos-ecmascript/) |
| `JS-10` | [Erros e Exceções](../practice/js-10-erros-e-excecoes/) |
| `JS-11` | [Assíncronismo e Promises](../practice/js-11-assincronismo-e-promises/) |
| `JS-12` | [Async/Await e Event Loop](../practice/js-12-async-await-e-event-loop/) |

---

# JS-01 — Valores, Tipos e Avaliação de Expressões

## Objetivo

Compreender como JavaScript representa valores e executa expressões, incluindo conversão de tipos e lógica booleana.

## Unidades

### JS-01.01 — Tipos Primitivos e Objetos

**Objetivo**

Distinguir os diferentes tipos primitivos (undefined, null, boolean, number, BigInt, string, Symbol) e valores de referência (objetos, arrays, funções) em JavaScript.

**Fundamentos**

- **Tipos primitivos:** características de `undefined`, `null`, Booleanos, números (e `NaN`, `Infinity`), BigInt, strings, Symbol.
- **Objetos como valores de referência:** criação de objetos literais, valores de referência, identidade dos objetos.
- **Operador `typeof`:** identifica tipos primitivos (atenção: `typeof null` é "object").

**Competências**

- Identificar o tipo de qualquer valor (`typeof`).
- Distinguir primitives de objetos/arrays/funções.
- Prever como valores especiais (`null`, `undefined`, `NaN`) se comportam em expressões.

**Dependências**

- Nenhuma (conteúdo básico).

**Web Integration**

Exibir o tipo ou valor recebido de um campo de formulário no console usando `typeof`, mostrando ao usuário se o valor inserido é número, texto, etc.

### JS-01.02 — Conversão de Tipos e Coerção

**Objetivo**

Entender como JS converte valores entre tipos em expressões e condições.

**Fundamentos**

- **Coerção implícita:** concatenação string + número, comparação `==`.
- **Truthy/Falsy:** valores que avaliam como false em condicionais (false, `undefined`, `null`, `0`, `NaN`, `""`); todos os demais (incluindo objetos) são truthy.
- **Conversão explícita:** `Boolean()`, `String()`, `Number()`.
- **Igualdade:** diferenças entre `==` (com coerção) e `===` (sem coerção).
- **Comparações numéricas e de string:** comportamento de `<`, `>` com diferentes tipos.

**Competências**

- Avaliar expressões que envolvem conversão de tipo (por exemplo, `'5' + 2` ou `5 == '5'`).
- Prever resultados de condicionais sabendo quais valores são truthy ou falsy.
- Justificar por que `null == undefined` é true, mas `null === undefined` é false.

**Dependências**

- JS-01.01 (conceitos de valor e tipo).

**Web Integration**

Implementar validação simples: por exemplo, ler um input numérico como texto e converter para número com `Number()`; verificar se a conversão falhou (`NaN`) antes de usar o valor.

## Checklist

Ao concluir este bloco, devo conseguir:

- [ ] Distinguir cada tipo primitivo e explicar casos peculiares (`typeof null`, `NaN`).
- [ ] Prever o valor resultante de expressões que envolvem diferentes tipos (concatenar string/número, operações booleanas).
- [ ] Determinar se um valor é truthy ou falsy em um `if`.
- [ ] Justificar o comportamento de `==` vs `===` em exemplos concretos.

## Validação

Avaliar se o aluno consegue, dado um trecho de código com operações e comparações, explicar por que cada resultado ocorre (incluindo conversão de tipo) e corrigir erros comuns de coerção.

# JS-02 — Bindings, Declarações e Escopo Léxico

## Objetivo

Entender como variáveis e funções recebem nomes no código e como esses nomes são associados a valores durante a execução.

## Unidades

### JS-02.01 — Declarações `var`, `let` e `const`

**Objetivo**

Conhecer diferenças fundamentais entre `var`, `let` e `const`, incluindo escopo e hoisting.

**Fundamentos**

- **Hoisting de `var`:** declarações de `var` são içadas ao topo da função (ou global) e inicializadas com `undefined`.
- **Escopo de bloco (`let`/`const`):** variáveis declaradas com `let` ou `const` só existem no bloco `{}` em que são definidas.
- **TDZ (Temporal Dead Zone):** `let` e `const` só são inicializadas no momento da declaração; acessar antes causa erro de referência.
- **Reatribuição:** `const` cria bindings imutáveis (identificador constante), diferentemente de `let`.

**Competências**

- Prever o valor de variáveis declaradas com `var` quando usadas antes da declaração (resultando em `undefined`).
- Identificar erros de referência quando um `let`/`const` é acessado antes de definido.
- Reescrever código para evitar vazamento acidental de variáveis globais (por exemplo, mudando `var` para `let`).

**Dependências**

- JS-01 (valores tipos básicos).

**Web Integration**

Implementar um contador simples usando `let` dentro de um evento de clique; demonstrar que a variável não existe fora da função (evitando poluir escopo global).

### JS-02.02 — Escopo Léxico e Shadowing

**Objetivo**

Explicar como as funções criam novos escopos e como a resolução de nomes ocorre (lookup léxico).

**Fundamentos**

- **Escopo de função:** cada função (declarada ou expressa) cria um novo ambiente léxico para seus parâmetros/variáveis.
- **Escopo global:** declarações fora de funções definem bindings globais (no `globalThis`).
- **Shadowing:** variáveis internas podem ocultar (shadow) variáveis externas com mesmo nome.
- **Ambientes léxicos:** modelo de cadeia de contextos onde cada referência é resolvida no escopo atual ou, se não existir, nos escopos superiores até o global.

**Competências**

- Determinar qual valor uma referência de variável acessa, em presença de variáveis com mesmo nome em escopos aninhados.
- Explicar por que determinada variável é ou não visível em cada parte do código.
- Reorganizar código para evitar conflitos de nome e dependências implícitas de escopo.

**Dependências**

- JS-02.01 (entendimento de `var`/`let`).

**Web Integration**

Exibir dinamicamente múltiplas mensagens distintas usando variáveis de mesmo nome em diferentes funções de eventos (por exemplo, nome do usuário em formulário vs em função de limpeza).

## Checklist

Ao concluir este bloco, devo conseguir:

- [ ] Explicar o que acontece ao acessar uma variável declarada com `var` antes da linha de declaração (hoisting).
- [ ] Identificar onde ocorrem erros de TDZ em código que usa `let`/`const`.
- [ ] Rastrear referências de variáveis em funções aninhadas, indicando qual escopo define cada binding.
- [ ] Prever como mudar `var` para `let`/`const` pode alterar o comportamento de loops e temporização (por exemplo, em laços `for`).

## Validação

O checkpoint deve apresentar um código com múltiplas declarações de `var` e `let` dentro de blocos e funções, pedindo ao estudante para apontar valores/erros resultantes e reescrever usando `let` adequadamente.

# JS-03 — Funções e Closures

## Objetivo

Explorar funções como valores de primeira classe em JavaScript e o mecanismo de closures que elas criam.

## Unidades

### JS-03.01 — Declaração, Expressão e Arrow Functions

**Objetivo**

Diferenciar as formas de criar funções em JavaScript e compreender que funções são valores.

**Fundamentos**

- **Funções de primeira classe:** uma função pode ser atribuída, passada ou retornada como valor. Isso habilita callbacks e funções de ordem superior.
- **Declarações vs Expressões:** diferença entre `function nome() {}` (função nomeada) e `const nome = function(){}` ou arrow (`=>`) (função anônima atribuída).
- **Arrow functions:** sintaxe compacta; **não** cria novo escopo de `this` (captura o `this` léxico).
- **Parâmetros e retorno:** comportamento de parâmetros opcionais, valores default; retorno implícito em arrow de expressão única.

**Competências**

- Escrever funções usando declaração e expressão (incluindo arrow) para o mesmo propósito, sabendo como as diferenças afetarão `this` e `arguments`.
- Passar funções como argumentos (callbacks) e receber funções de outras funções (higher-order).
- Converter uma função tradicional em arrow function onde aplicável, ou vice-versa, preservando funcionalidade.

**Dependências**

- JS-01 (tipos); JS-02 (escopo).

**Web Integration**

Criar um manipulador de evento de clique passado como função de callback; observar como `this` (evento) é tratado dentro do handler quando escrito como função normal vs arrow.

### JS-03.02 — Escopo Léxico e Closures

**Objetivo**

Compreender o escopo léxico de funções e como closures preservam variáveis do contexto de criação.

**Fundamentos**

- **Escopo léxico:** cada função “fecha sobre” o ambiente em que foi definida.
- **Closure:** quando uma função interna referencia variáveis do escopo externo, essas variáveis permanecem acessíveis mesmo após o término da execução externa.
- **Estado privado:** uso de closures para manter estado entre chamadas (padrões como contador), sem expor variáveis globalmente.
- **Lifetime dos bindings:** variáveis em closures só são coletadas se não houver mais referência à função ou ao próprio binding.

**Competências**

- Prever quais variáveis cada função aninhada pode acessar, dado um exemplo de múltiplos níveis de função.
- Usar closures para implementar padrões (por exemplo, função que retorna outra função que incrementa um contador interno).
- Identificar e corrigir bugs comuns de closure, como o “capturar laço com var” (falha em closures dentro de loops usando `var`).

**Dependências**

- JS-03.01 (formação de funções); JS-02.02 (escopo léxico).

**Web Integration**

Implementar um contador clicável que mantém o número de cliques em um closure (por exemplo, `let count=0; return () => {count++; ...}`), demonstrando persistência de estado privado.

## Checklist

Ao concluir este bloco, devo conseguir:

- [ ] Demonstrar que uma função é um valor: armazená-la em variável, passá-la e retorná-la de outra função.
- [ ] Traçar o escopo léxico: dada função fechada, listar todas as variáveis externas que ela “fecha” (closure).
- [ ] Prever o resultado de código com callbacks e closures (por exemplo, chamar sequencialmente várias funções geradas por outra).
- [ ] Escrever uma closure que mantenha estado entre chamadas (como factory de funções com estado privado).

## Validação

Avaliar se o estudante pode refatorar um uso de callback dentro de uma função para usar closures de forma adequada, explicando por que o estado foi ou não preservado.

# JS-04 — Objetos: Propriedades, Referências e Mutabilidade

## Objetivo

Investigar o modelo de objeto JavaScript: criação, acesso e efeitos da identidade e referência.

## Unidades

### JS-04.01 — Criação e Acesso a Propriedades

**Objetivo**

Saber criar objetos, adicionar/acessar propriedades e entender como atualizações são feitas.

**Fundamentos**

- **Sintaxe de objeto:** inicializadores literais `{ chave: valor }` e `new Object()`.
- **Propriedades:** acesso por notação de ponto e colchetes; chaves strings/symbols; definições padrão (enumerable, writable, etc.).
- **Inserção/atualização:** atribuir `obj.propriedade = novoValor` cria ou atualiza; adicionar métodos (funções como propriedades).
- **Nomes computados e símbolos:** usar expressões ou símbolos como chaves quando necessário.

**Competências**

- Escrever literais de objeto com múltiplas propriedades/métodos; acessar dinamicamente propriedades usando variáveis.
- Prever o estado do objeto após operações de criação/atualização (incluindo aninhamento de objetos).
- Diagnosticar acesso incorreto (por exemplo, colchetes vs ponto para chaves não-identificadores).

**Dependências**

- JS-03 (funções como métodos de objeto).

**Web Integration**

Representar no JS um registro de formatação (por exemplo, um objeto `user` com nome e email) e atualizar seus campos conforme entradas do usuário, refletindo alterações no UI ou no console.

### JS-04.02 — Identidade, Referência e Mutabilidade

**Objetivo**

Entender que objetos são armazenados por referência, como compartilhar e copiar seu conteúdo.

**Fundamentos**

- **Identidade de objeto:** cada objeto tem identidade única; atribuir a outra variável cria outra referência para o mesmo objeto.
- **Comparação:** comparação de objetos com `==`/`===` só verifica identidade (mesmo objeto), não estrutura.
- **Mutabilidade:** alterar um objeto afeta todas as referências.
- **Cópias rasas:** duplicar objeto/array superficialmente (`Object.assign`, spread `{...obj}`), sabendo que isso copia referências internas.
- **Cópias profundas:** nota sobre necessidade (não embutida em JS, requer manual ou API).
- **Objetos aninhados:** atenção especial, pois referências internas também podem ser compartilhadas.

**Competências**

- Prever efeitos de aliasing: dado código onde múltiplas variáveis referenciam o mesmo objeto, apontar como uma mudança será vista em todas.
- Implementar cópia rasa de objeto/array; explicar por que propriedades aninhadas ainda ficam compartilhadas.
- Identificar bugs de mutação involuntária (por exemplo, array copiado por atribuição e modificado em outro escopo).

**Dependências**

- JS-04.01 (acesso a objetos); JS-01 (valores vs referências).

**Web Integration**

Manusear uma lista de itens em um objeto (ou array) compartilhado entre funções de callback (e.g. adicionar/remover itens num carrinho de compras), observando efeitos de referência.

## Checklist

Ao concluir este bloco, devo conseguir:

- [ ] Mostrar que duas variáveis que apontam para o mesmo objeto compartilham estado: modificar via uma altera o outro.
- [ ] Determinar quando fazer cópia rasa (`{...obj}` ou `arr.slice()`) para evitar mutação indesejada; apontar quando ainda existe compartilhamento interno.
- [ ] Distinguir igualdade de valor de igualdade de referência em objetos e arrays.
- [ ] Diagnosticar e corrigir código que acidentalmente conflita ao usar um objeto mutável (por exemplo, clonando antes de modificar).

## Validação

Apresentar um cenário onde dois componentes JS manipulam o mesmo objeto global e pedir para identificar consequências de compartilhamento; corrigir usando cópia.

# JS-05 — Protótipos, Herança e Classes

## Objetivo

Estudar o mecanismo de herança prototípica de JavaScript e a sintaxe de classes que o abstrai.

## Unidades

### JS-05.01 — Cadeia de Protótipos

**Objetivo**

Compreender como objetos podem herdar propriedades via protótipos.

**Fundamentos**

- **Prototype chain:** todo objeto criado (literal, array, função) tem um link `[[Prototype]]` para outro objeto padrão (e.g., `Array.prototype`, `Object.prototype`).
- **Lookup de propriedade:** ao acessar `obj.prop`, JS procura primeiro em `obj`; se não encontrar, vai para `obj.[[Prototype]]` e assim por diante até null.
- **Alterando protótipos:** uso de `Object.create`, `__proto__`, ou definindo propriedades em `Constructor.prototype` para afetar instâncias futuras.
- **Herança de comportamento:** dar exemplos onde métodos nativos (como `toString`) vem de `Object.prototype`.

**Competências**

- Rastrear onde uma propriedade/método é encontrado em um objeto ou em sua cadeia (detalhar a sequência de busca).
- Escolher entre definir método diretamente no objeto ou no protótipo, justificando impacto na herança.
- Evitar armadilhas de herança, por exemplo, entender que alterar um protótipo afeta todas as instâncias.

**Dependências**

- JS-04 (objetos e propriedades).

**Web Integration**

Criar uma cadeia prototípica customizada: por exemplo, definir `Animal` como função construtora e adicionar método a `Animal.prototype`, instanciar e usar método herdado em instâncias (animais diferentes).

### JS-05.02 — Classes e Herança de Classes

**Objetivo**

Entender a sintaxe `class` e sua relação com o modelo de protótipos.

**Fundamentos**

- **Sintaxe `class`:** declaração de classe com `constructor`, métodos, `extends`, `super`.
- **Instâncias:** uso de `new` para criar objetos cuja `[[Prototype]]` é a função `constructor.prototype`.
- **Herança de classes:** `class Sub extends Base` faz `Sub.prototype.[[Prototype]] = Base.prototype`.
- **Classes são açúcar sintático:** internamente equivalem a função construtora + protótipo; métodos definidos na classe são não-enumeráveis.

**Competências**

- Definir uma classe JS com construtor e métodos; criar instâncias e acessar métodos herdados.
- Desenhar uma hierarquia simples de classes (`extends`) e explicar como o protótipo é encadeado.
- Comparar código equivalente entre sintaxe de classe e funções construtoras + protótipo, reconhecendo semântica igual.

**Dependências**

- JS-05.01 (protótipos); JS-03 (funções construtoras tratadas como funções normais).

**Web Integration**

Modelar entidades de uma aplicação web com classes: por exemplo, criar classes `Card`, `Deck` ou `Usuario` para gerenciar dados do front-end e instanciar objetos.

## Checklist

Ao concluir este bloco, devo conseguir:

- [ ] Explicar passo a passo onde `obj.prop` é buscado quando `obj` tem um protótipo customizado.
- [ ] Estabelecer uma relação de herança utilizando protótipos ou `class extends`, sabendo como os métodos são compartilhados.
- [ ] Diferenciar efeitos de definir um método em `constructor.prototype` vs diretamente na instância.
- [ ] Dado um exemplo em `class`, reescrever de forma equivalente usando funções construtoras e vice-versa.

## Validação

Pedir para o estudante criar duas classes relacionadas (herança prototípica) e justificar como métodos são encontrados em cada instância, ou depurar herança incorreta.

# JS-06 — Métodos e `this`

## Objetivo

Elucidar como o contexto de invocação (`this`) é determinado e como usá-lo corretamente em métodos e callbacks.

## Unidades

### JS-06.01 — Chamada de Método e Contexto de `this`

**Objetivo**

Entender como o modo de chamar uma função define o valor de `this`.

**Fundamentos**

- **Chamada de método:** `obj.metodo()` vincula `this` a `obj`. Mesmo se `metodo` vier de um protótipo, o contexto é o objeto que fez a chamada.
- **Função solta:** chamar `func()` isoladamente (sem objeto) define `this` como `undefined` (modo estrito) ou `globalThis` (modo não estrito).
- **Call, apply, bind:** métodos para chamar explicitamente `this` em uma função.
- **Perda de contexto:** passar método de objeto como callback pode “perder” o `this` original (muda para indefinido/global se não for restrito).

**Competências**

- Prever o valor de `this` em diferentes formas de invocação: `obj.metodo()`, `metodo()` descarregado, ou `metodo.call(outro)`.
- Resolver cenários comuns de perda de `this` (por exemplo, armazenar `const f = obj.metodo; f()`; ou usar em callback de evento DOM).
- Usar `bind` ou closures para preservar o contexto adequado quando necessário.

**Dependências**

- JS-05 (objetos e métodos).

**Web Integration**

Criar um botão `<button>` cujo manipulador chama um método de um objeto; mostrar que, sem bind, o `this` dentro do método é o elemento do DOM, e com arrow/bind pode ser o objeto desejado.

### JS-06.02 — Arrow Functions e `this` Lexical

**Objetivo**

Destacar como arrow functions tratam `this` diferente das funções tradicionais.

**Fundamentos**

- **Arrow e `this`:** arrow não cria um novo `this`; ele herda (`fecha sobre`) o `this` do contexto léxico em que foi definido.
- **Imutabilidade de `this` em arrow:** nem `call/apply/bind` alteram o `this` em arrow (são ignoradas).
- **Uso comum:** arrow é útil para callbacks onde queremos usar `this` do escopo externo (por exemplo, em métodos de classe para callbacks de event).

**Competências**

- Decidir quando usar arrow function para evitar rebinding de `this` (por exemplo, em closures de métodos).
- Explicar por que `this` permanece o mesmo (lexical) em arrow functions, ilustrando em código aninhado.
- Reconhecer que arrow não serve como construtora (`new` com arrow é erro).

**Dependências**

- JS-03.01 (arrow functions sintaxe); JS-06.01 (conceito geral de `this`).

**Web Integration**

Exemplificar em código de componente front-end (por exemplo, callback de evento ou método de objeto) usando função arrow para que `this` continue sendo o objeto desejado, evitando `undefined`.

## Checklist

Ao concluir este bloco, devo conseguir:

- [ ] Determinar o valor de `this` em uma chamada de método e em uma função normal invocada sem contexto.
- [ ] Corrigir problemas em callbacks de objeto (por exemplo, passar método de classe para evento HTML) usando `bind` ou arrow.
- [ ] Justificar o comportamento de `this` em arrow functions (`sempre o `this` léxico`).
- [ ] Reconhecer situações onde `this` é `undefined` e como o modo estrito evita vazamento para `globalThis`.

## Validação

Apresentar código onde métodos perdem seu contexto (e.g. sejam passados como callback) e exigir que o estudante indique o problema de `this` e corrija usando bind ou arrow function, explicando a mudança.

# JS-07 — Coleções e Iteração (Arrays e Iteráveis)

## Objetivo

Cobrir coleções nativas de JavaScript (principalmente arrays e strings) e os padrões de iteração sobre elas.

## Unidades

### JS-07.01 — Arrays, Strings e Métodos Essenciais

**Objetivo**

Entender arrays (e imutabilidade relativa de strings) como coleções, e usar métodos comuns de transformação.

**Fundamentos**

- **Arrays:** são objetos indexados (chaves numéricas); possuem propriedade `length` dinâmica. Atribuir a índices (mesmo além do atual `length`) ajusta automaticamente o tamanho.
- **Strings:** sequências imutáveis de caracteres. Indexação produz caracteres e permite iteração. Possuem métodos próprios (slice, toUpperCase, etc.).
- **Métodos de array:** mutadores (`push`, `pop`, `splice`, etc.) versus não-mutadores (`map`, `filter`, `slice`). Usar `map/filter` para processamento declarativo e evitar mudança de estado global.
- **Spread e rest para coleções:** espalhar (`...array`) para copiar ou concatenar; coletar em parâmetros (`...args`). Desestruturação básica de arrays e strings.

**Competências**

- Prever o resultado de operações de array, incluindo métodos mutáveis vs não-mutáveis.
- Reescrever loops tradicionais usando métodos de array (`map`, `filter`) quando adequado.
- Aplicar desestruturação de array e spread para clonar ou extrair partes de arrays/strings.

**Dependências**

- JS-04 (objetos e mutabilidade).

**Web Integration**

Consumir uma lista de dados (p.ex. itens de um JSON) usando `fetch` em uma função assíncrona e preencher elementos `<li>` via `map`; ou usar `filter` para destacar itens que cumprem certo critério na página.

### JS-07.02 — Iteração e Iteráveis

**Objetivo**

Aprender a iterar de forma geral sobre estruturas de coleção e outros iteráveis.

**Fundamentos**

- **Loops tradicionais:** `for`, `while`, mas enfatizar `for...of` para arrays e iteráveis (objetos que implementam `@@iterator`).
- **for...in vs for...of:** para objetos genéricos, `for-in` itera chaves enumeráveis, mas para arrays recomenda-se `for-of`.
- **Iteradores e geradores:** menção ao protocolo de iteração (`Symbol.iterator`) e iteráveis padrão (`Array`, `String`, `Map`, `Set`, etc.).
- **Atenção a mutações durante iteração:** explicar como modificar array dentro do loop pode afetar resultados.

**Competências**

- Escolher o laço adequado a cada situação: percorrer índices, percorrer valores ou chaves de objeto.
- Usar `for...of` com arrays e strings, entender que percorre valores (iteração sequencial).
- Iterar sobre objetos (via `Object.keys` ou `for...in`) corretamente.

**Dependências**

- JS-04 (objetos, coleções); JS-07.01 (arrays).

**Web Integration**

Por exemplo, iterar sobre um `HTMLCollection` ou `NodeList` (que são iteráveis) usando `for...of`, para atribuir event listeners a múltiplos elementos de forma simples.

## Checklist

Ao concluir este bloco, devo conseguir:

- [ ] Diferenciar métodos que mutam arrays (push, pop etc.) de métodos que retornam novo array (map, filter, slice).
- [ ] Resolver tarefas de processamento de coleção com métodos funcionais (map/filter/reduce), explicando como evitam mutações manuais.
- [ ] Iterar coleções usando `for...of` ou `forEach`, explicando a sequência de acesso a elementos.
- [ ] Evitar iterar objetos (não-iteráveis) com `for...of` (usar `Object.entries` ou `for...in` nesse caso).

## Validação

Propor um cenário de manipulação de array onde o aluno deve escolher entre loop explícito e métodos de array, justificando a escolha, além de iterar sobre elementos do DOM replicando sua funcionalidade em código JS.

# JS-08 — Recursos Modernos da Linguagem

## Objetivo

Familiarizar-se com sintaxes modernas e úteis do ES6+ que complementam o modelo mental geral.

## Unidades

### JS-08.01 — Destructuring, Spread e Rest

**Objetivo**

Aprender as sintaxes de desempacotamento e agregação de valores.

**Fundamentos**

- **Destructuring de array e objeto:** extrair valores de um array/objeto diretamente em variáveis.
- **Parâmetros rest:** coletar múltiplos argumentos em um array (funções variádicas).
- **Operator spread:** espalhar elementos de array ou propriedades de objeto em literal, copia rasa e concatenar.
- **Valores padrão:** definir padrão para parâmetros de função ou em destructuring.

**Competências**

- Reescrever atribuições manuais de elementos de arrays/objetos usando destructuring para código mais conciso.
- Utilizar spread para clonar estruturas ou passar elementos de array como argumentos (por exemplo, `func(...arr)`).
- Aplicar rest em funções para lidar com número variável de argumentos.

**Dependências**

- JS-04 (objetos, arrays); JS-07 (arrays).

**Web Integration**

Usar destructuring para extrair dados retornados de uma `fetch` (por exemplo, `const {id, title} = post`) e preenchê-los no DOM.

### JS-08.02 — Outros Recursos: Template Literals, Optional Chaining, Nullish Coalescing

**Objetivo**

Conhecer sintaxes adicionais frequentes em código moderno.

**Fundamentos**

- **Template literals:** strings delimitadas por acento grave, permitem interpolação `${...}` e multilinhas.
- **Optional chaining (`?.`):** acessar propriedades aninhadas sem erro se algum nível for `null`/`undefined`.
- **Nullish coalescing (`??`):** operar parecido com `||` mas somente consideram `null`/`undefined` como “vazios”.
- **Default parameters** (reforço): garantir valor padrão em parâmetros de função.

**Competências**

- Construir strings complexas sem concatenação manual usando template literals.
- Proteger acessos a propriedades de objetos que podem ser nulos usando `?.`.
- Diferenciar `||` de `??` ao definir valores default (entender que `||` considera `0` e `""` como falsy, enquanto `??` não).

**Dependências**

- JS-01 (valores null/undefined); JS-08.01 (spread/rest para casos similares).

**Web Integration**

Criar strings de marcação HTML com template literals inserindo variáveis; acessar dados aninhados de objetos de resposta (por exemplo, `resp.data?.user?.name`) sem erro caso algo não exista.

## Checklist

Ao concluir este bloco, devo conseguir:

- [ ] Usar destructuring para extrair múltiplos valores de arrays/objetos em variáveis de forma limpa.
- [ ] Aplicar spread/rest para simplificar manipulação de argumentos e clonagem de coleções.
- [ ] Compor strings complexas usando template literals em vez de concatenação (`+`).
- [ ] Usar `?.` para evitar erros ao acessar campos profundos que podem ser indefinidos, e `??` para valores default precisos.

## Validação

Exercícios pediriam reescrever código com concatenação/if em versões usando estes recursos (por exemplo, acessar propriedade aninhada com `?.` ou construir mensagem com template literal), justificando as melhorias.

# JS-09 — Módulos ECMAScript

## Objetivo

Ensinar o sistema de módulos padrão do JavaScript moderno para organização de código em arquivos.

## Unidades

### JS-09.01 — `export` e `import`

**Objetivo**

Compreender a sintaxe básica de exportação e importação de valores entre módulos.

**Fundamentos**

- **Exportações nomeadas e default:** `export {val1, val2}` vs `export default`, e `import {val1} from` vs `import valDefault from`.
- **Bindings estáticos:** importações criam referências vivas aos valores exportados (read-only local).
- **Escopo de módulo:** cada arquivo é executado em seu próprio escopo; não polui global.
- **Carregamento em browsers:** uso de `<script type="module">` e caminhos relativos para arquivos JS.

**Competências**

- Configurar dois arquivos JS onde um exporta funções/valores e outro importa usando `import`.
- Escolher entre export default ou nomeados dependendo do caso de uso (objeto utilitário vs módulo single feature).
- Prever erros comuns: esquecer `export`, usar nome errado em import, ou não incluir `.js` no caminho.

**Dependências**

- JS-03 (funções a serem exportadas); JS-07 (arrays ou objetos exportáveis como dados).

**Web Integration**

Criar um módulo `utils.js` que exporta funções de formatação de data e importar em `main.js` para formatar uma data na página.

### JS-09.02 — Módulos em Prática

**Objetivo**

Entender carregamento e avaliação de módulos em cenário real.

**Fundamentos**

- **Módulos vs scripts clássicos:** módulos são “deferidos” por padrão, têm escopo próprio e são avaliados uma vez.
- **Import maps (opcional):** breve menção de como especificar caminhos personalizados em browsers modernos.
- **Dependências cíclicas:** noções básicas do que pode dar errado se dois módulos se importam mutuamente (posições de execução).
- **Modularização:** benefícios de encapsular código em módulos, evitando variáveis globais e facilitando manutenção.

**Competências**

- Integrar módulos em um HTML real usando `<script type="module">`.
- Diagnosticar problemas de importação em aplicações de múltiplos arquivos (ex: ordem de carregamento, erros de console sobre módulos).
- Explicar por que módulos permitem compartilhar código sem `window.` e como a reutilização é facilitada.

**Dependências**

- JS-09.01.

**Web Integration**

Construir página HTML que importa módulos JS: por exemplo, `index.html` carrega `app.js` que por sua vez importa funções de `domUtils.js` e `data.js` para montar conteúdo da página.

## Checklist

Ao concluir este bloco, devo conseguir:

- [ ] Configurar um pequeno projeto modular: criar um arquivo que exporta funções/constantes e outro que importa e usa essas features corretamente.
- [ ] Explicar a diferença entre usar `export default` e `export` nomeado, mostrando exemplos de cada.
- [ ] Prever como o código é avaliado: por exemplo, entender que módulos importados múltiplas vezes não duplicam execução do código.
- [ ] Resolver conflitos simples de import (caminho relativo errado, falta de extensão, conflito de nomes).

## Validação

Propor um conjunto de módulos com interdependências simples e pedir para o estudante organizar `import/export` para torná-los funcionais (sem poluir escopo global), além de explicar o fluxo de carregamento.

# JS-10 — Erros e Exceções

## Objetivo

Mostrar como tratar erros em JavaScript como parte do fluxo normal de execução.

## Unidades

### JS-10.01 — `throw` e Objeto `Error`

**Objetivo**

Aprender a gerar erros propositais e usar objetos de erro padrão.

**Fundamentos**

- **Instrução `throw`:** lança uma exceção imediatamente, interrompendo o fluxo atual; qualquer expressão pode ser lançada.
- **Objetos `Error`:** criação de novos erros personalizados (`new Error("mensagem")` ou subtipos como `TypeError`). Diferenciação entre lançar string vs objeto (boa prática usar objetos).
- **Propagação de erro:** exceções não tratadas sobem a pilha até o próximo `catch` ou terminam o programa.

**Competências**

- Usar `throw new Error("msg")` para validar argumentos de função e sinalizar condições inválidas.
- Criar erros específicos (por exemplo, `throw new RangeError()` para índices fora de faixa).
- Entender que, em funções assíncronas (promises, callbacks), `throw` rejeita a promise automaticamente.

**Dependências**

- JS-01 (valores de erro); JS-03 (funções para lançar).

**Web Integration**

No contexto de formulário, validar dados e lançar um erro com `throw` quando o usuário envia informação inválida (por exemplo, formato de email), então capturar esse erro para exibir uma mensagem ao usuário.

### JS-10.02 — `try...catch...finally`

**Objetivo**

Aprender a capturar e tratar exceções durante a execução de blocos de código.

**Fundamentos**

- **Estrutura `try/catch`:** bloco `try` contém código “perigoso”; se ocorre `throw`, a execução pula para o `catch`. Se nenhum erro ocorre, `catch` é ignorado.
- **`finally`:** bloco opcional que é executado após `try`/`catch`, sempre (usado para limpeza).
- **Escopo de captura:** variáveis definidas em `catch (e)` só existem dentro do `catch`.
- **Re-throw:** em `catch` pode-se lançar novamente erro para propagar.

**Competências**

- Envolver trechos de código suscetíveis a erro (como parse JSON ou operações que podem falhar) em `try/catch`.
- Extrair informações do objeto de erro capturado (`e.message`, `e.name`, `e.stack`) para log/diagnóstico.
- Decidir quando tratar o erro no local ou re-lançar para quem chamou.

**Dependências**

- JS-10.01 (lançamento de erros).

**Web Integration**

Fazer `try { JSON.parse(input) } catch(e) { alert("JSON inválido") }` ao receber entrada do usuário, demonstrando tratamento de erros de parsing.

## Checklist

Ao concluir este bloco, devo conseguir:

- [ ] Usar `throw` para sinalizar condições inválidas (como index fora de faixa) e explicar que isso interrompe o fluxo.
- [ ] Capturar exceções com `try...catch`, distinguindo código normal do tratamento de erro.
- [ ] Garantir que um bloco `finally` seja executado em todas as situações (útil para limpeza de recursos).
- [ ] Demonstrar como re-encadear um erro (`throw` dentro do `catch`) após adicionar informação extra.

## Validação

Apresentar função que pode gerar erro e pedir para o estudante cercar de `try/catch`, além de explicar o que acontece quando `throw` é usado dentro do `try`.

# JS-11 — Assíncronismo e Promises

## Objetivo

Introduzir o modelo de programação assíncrona usando callbacks e consolidar o conceito de Promise para controlar fluxo assíncrono.

## Unidades

### JS-11.01 — Callbacks e Fluxo Assíncrono

**Objetivo**

Entender o padrão antigo de callbacks para operações assíncronas.

**Fundamentos**

- **Callbacks:** passar função para ser executada ao fim de operação assíncrona (por exemplo, `setTimeout(fn, ms)` ou um pedido AJAX).
- **Problemas de callback:** múltiplos callbacks aninhados (“callback hell”) dificultam leitura e tratamento de erros.
- **Sequenciamento assíncrono:** como evitar condições de corrida garantindo que callbacks sejam chamados na ordem desejada.

**Competências**

- Registrar múltiplos callbacks e prever a ordem de execução baseada nos tempos/delays.
- Transformar código com callbacks aninhados em uma sequência linear usando técnicas como funções encadeadas.
- Identificar onde callbacks podem falhar silenciosamente e a importância de funções de erro (ex. callback(err, data)).

**Dependências**

- JS-06 (this, pois callbacks de `this` em métodos podem perder contexto).

**Web Integration**

Configurar `setTimeout` ou `setInterval` para atualizar elementos DOM após atrasos, provando que o resto do script continua executando sem bloqueio.

### JS-11.02 — Promises: Estado e Encadeamento

**Objetivo**

Aprender o uso de Promises para representar operações assíncronas de forma encadeável e estruturada.

**Fundamentos**

- **Criação de Promise:** `new Promise((resolve, reject) => {...})`.
- **Estados da Promise:** `pending`, `fulfilled` (resolvida com valor), `rejected` (erro).
- **`then`, `catch`, `finally`:** encadeamento de tratamento: `then(onFulfilled, onRejected)` adiciona callbacks que serão chamados quando a promise resolver; `catch` é atalhos para tratar erros; `finally` executa independente do resultado.
- **Encadeamento:** `then()` retorna uma nova promise permitindo sequenciar ações. Erros não tratados sobem até o próximo `catch`.
- **Evitar callback hell:** comparar estrutura de encadeamento de promises (flat) com aninhamento de callbacks.

**Competências**

- Converter código assíncrono baseado em callback para usar Promises (`resolve` e `reject`).
- Encadear várias operações assíncronas: usar `then` sequencialmente para processar resultados intermediários, assegurando fluxo correto.
- Lidar com erros em cadeia: observar como lançar/exceção dentro de `then` pula para o próximo `catch`.
- Conhecer métodos estáticos úteis (`Promise.all`, `Promise.resolve`, etc.) em nível básico.

**Dependências**

- JS-11.01 (conceito de fluxo assíncrono).

**Web Integration**

Fazer uma requisição com a API `fetch` (retorna Promise) para trazer dados de uma API pública e então encadear `.then()` para processar JSON e atualizar a página. Demonstrar `catch` para erro de rede.

## Checklist

Ao concluir este bloco, devo conseguir:

- [ ] Criar uma `Promise` manualmente e disparar `resolve` ou `reject` de dentro dela.
- [ ] Usar `.then()` e `.catch()` para encadear ações após uma operação assíncrona, explicando o fluxo de valores e erros.
- [ ] Comparar duas sequências assíncronas (callback vs promise) e justificar qual é mais legível/manutenção.
- [ ] Desenhar o fluxo de execução: entender que `.then()` retorna outra promise e que múltiplos `then` são executados na ordem em que foram definidos.

## Validação

Fornecer código com promessas simples (como `fetch` ou `setTimeout`) e pedir para ordenar/explicar as saídas, além de reescrever aninhamento de callbacks em promises com `then`.

# JS-12 — Async/Await e Event Loop

## Objetivo

Aprender `async/await` como sintaxe de açúcar sobre Promises e compreender o modelo de execução assíncrona (event loop, tasks/microtasks).

## Unidades

### JS-12.01 — `async`/`await` e Fluxo Assíncrono

**Objetivo**

Entender como usar `async`/`await` para escrever código assíncrono de maneira síncrona e os cuidados relacionados.

**Fundamentos**

- **Funções `async`:** toda função marcada `async` retorna automaticamente uma Promise. O valor retornado é tratado como resolução da promise (valor implícito é encapsulado com `Promise.resolve`).
- **Operador `await`:** só pode ser usado dentro de `async`; pausa execução da função até a Promise ser resolvida ou rejeitada. O valor após `await` é o resultado da promise.
- **Erros com `await`:** se a promise rejeitar, um erro é lançado no ponto do `await`, podendo ser capturado por `try/catch`.
- **Paralelismo vs Sequência:** chamar `await` sequencialmente serializa as operações; múltiplos `await` independentes podem (às vezes devem) ser iniciados em paralelo e depois aguardados juntos (`Promise.all`) para melhorar desempenho.
- **Limitações:** demonstrar que `await` não bloqueia todo o programa, apenas “pausa” a função assíncrona, e que outros códigos (microtasks) podem continuar antes do próximo `await`.

**Competências**

- Refatorar cadeias de `then` para usar `async`/`await`, simplificando a legibilidade.
- Reconhecer quando não é necessário usar `await` (por exemplo, se não precisa do valor retornado imediatamente), evitando operações serializadas desnecessárias.
- Usar `try/catch` dentro de função `async` para tratamento de erros assíncronos.

**Dependências**

- JS-11 (Promises e encadeamento).

**Web Integration**

Criar uma função assíncrona que faz múltiplas requisições `fetch` em sequência usando `await`, por exemplo, obter perfil de usuário e depois suas postagens, atualizando a página passo a passo.

### JS-12.02 — Modelo de Execução e Event Loop

**Objetivo**

Explicar como o JavaScript executa código assíncrono sob a cobertura, focando em tasks, microtasks e ordenação de execução.

**Fundamentos**

- **Call stack e jobs:** tarefas (jobs) são empilhadas na fila e executadas até conclusão (run-to-completion).
- **Tasks vs Microtasks:** eventos assíncronos e callbacks normais formam tasks (macrotasks), enquanto callbacks de Promises são microtasks. Microtasks são processadas antes de continuar no próximo tick de tasks.
- **Sem bloqueio:** o loop de eventos garante que I/O (timers, XHR, fetch) ocorrem assincronamente; o código após uma operação assíncrona só roda via callback ou promise (like `then`).
- **Exemplo de ordenação:** ilustrar que Promise.resolve().then(...) sempre roda antes de setTimeout(..., 0).

**Competências**

- Descrever a ordem de execução entre código síncrono, `then` de promessa e callbacks de timers em um exemplo concreto.
- Prever resultados de código envolvendo múltiplos `setTimeout`, `Promise.then` e chamadas normais.
- Analisar brevemente porque `await` não interrompe eventos subsequentes pendentes: após `await`, o resto da função vira microtask.

**Dependências**

- JS-11/JS-12.01 (Promises e async/await).

**Web Integration**

Demonstrar em código front-end que atualizações via `setTimeout` e `Promise.then` ocorrem em ordem previsível: por exemplo, registrar no console a sequência de `console.log` no corpo principal, em um `.then()`, e em um `setTimeout`, verificando que `.then()` (microtask) executa antes do próximo tick de `setTimeout` (task).

## Checklist

Ao concluir este bloco, devo conseguir:

- [ ] Reescrever código de Promise em `async`/`await` corretamente, explicando que a função continua executando depois do `await` quando a Promise resolve.
- [ ] Identificar cenários onde `await` serializa desnecessariamente (e como paralelizar com `Promise.all`).
- [ ] Explicar o *Event Loop*: que cada job roda inteiro antes de outro começar (run-to-completion).
- [ ] Prever a ordem de execução envolvendo tasks e microtasks; por exemplo, saber que callbacks de promises (`then`) são executados antes de timers pendentes.

## Validação

Apresentar um trecho de código com várias operações assíncronas (mix de `await`, `then`, `setTimeout`) e pedir que o estudante indique a sequência de logs resultante, justificando pela teoria do event loop.

---

### Navegação

[← Mapa curricular](./README.md) ·
[↑ JavaScript Foundations Lab](../README.md) ·
[JS-01 — Valores, Tipos e Avaliação de Expressões →](../practice/js-01-valores-tipos-e-avaliacao-de-expressoes/)
