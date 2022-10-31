# Seletores

* Conecta um elemento HTML com o CSS a fim de alterar o elemento.

## Tipos

* Element selector
  - Todos os elementos HTML
* ID Selector
  - Um elemento que tenha o atributo `id`
  - Cada id deverá ser único
* Class Selector
  - Os elementos que contenham um atributo `class`
* Attribute Selector
  - Um elemento que contenha um atributo específico
  `[title] {}`
* Pseudo-class selector
  - Elementos em um estado específico

  ## Múltiplos

  * você poderá selecionar múltiplos elementos e aplicar alguma regra CSS ára todos eles. Usamos uma separação por vírgulas pra isso.

  ```css 
  h1, p, a {
    color: red;
  }
  ```

  # Combinators

  * Combinadores, pois eles trabalham para buscar e combinar seletores a fim de aplicar uma estilização.

  ## Descendant combinator

  * Identificado por um espaço entre os seletores.
  * Busca um elemento dentro de outro.

  ```css
  body article h2
  ```

  ## Child combinator

  * Identificado pelo sinal `>` entre dois seletores.
  * Seleciona somente o elemento que é filho direto do pai.
  * Elementos depois do filho direto serão desconsiderados.

  ```css
  body > ul > li
  ```

  `Obs: aplica somente ao primeiro.`

  ## Adjacent sibling combinator

  * Identificado pelo sinal `+` entre dois seletores.
  * Seleciona somente o elemento do lado direito que é irmão direto na hierarquia.

  ```css 
  h1 + p {
    color: blue;
  }
  ```

  ## General sibling combinator

  * Identificado pelo sinal `~` entre dois seletores.
  * Seleciona todos os elementos irmãos.

  ```css
  h1 ~ p
  ```

  `Todos os p que estão ao lado do h1.`

  ## Utilizando combinators

  ```css
  ul > li [class="red"]
  ```

  ## Dica

  * Seletores muito específicos tendem a causar dificuldades no reuso das regras de estilização dos elementos.
  * Muitas vezes, um simples uso de classes, torna o trabalho muito mais eficiente.