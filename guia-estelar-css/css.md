# CSS

### O que significa CSS?

* Cascading Style Sheet
* Código para criar estilos no HTML
* HTML é a estrutura, e o CSS é a beleza
* Não é uma linguagem de programação
* É uma linguagem style sheet

### Comentários

* Não irá afetar o seu código
* Ajuda a lembrar blocos de códigos
* Deixa dicas para leitura
* Ajuda outros a entenderem
* Nunca esqueça de fechar um comentário aberto
* Comentários começam com /* e terminam com */

### Anatomia

```css
h1 {
  color: blue;
  font-size: 60px;
  background: gray;
}
```

* Selector (h1)
* Declaration (tudo)
* Properties (várias propriedades)
* Property Value (valor da propriedade)

### Selectors

* Conecta um elemento HTML com o CSS

#### Tipos

* Global selector `*`
* Element/Type selector `h1, h2, p,div`
* ID Selector: `#box, #container`
* Class Selector: `.red, m-4`
* Attribute selector, Pseudo-class, Pseudo-element, etc

### Box Model

* Toda caixa tem seus limites, tem altura e largura, tem preenchimento, conteúdo, espaço entre elas

* Você irá perceber que (quase) tudo são caixas do CSS
* Posicionamentos, tamanhos, espaçamentos, bordas, cores
* Caixa pode ficar ao lado de uma outra, ou acima, abaixo
* Elementos HTML são caixas

### Adicionando CSS

#### inline

* atrbuto `style`

#### `<style>`

  * tag html que irá conter o css

#### `<link>`

* melhor prática
* arquivo css externo

#### `@import`

* utiliza dentro do css
* arquivo css externo

### Cascata (cascading)

* A escolha do browser de qual regra aplicar, caso haja muitas regras para o mesmo elemento.

* Seu estilo é lido de cima para baixo.

É levado em consideração 3 fatores:

1. Origem do estilo
2. Especificidade
3. Importância

#### Origem do estilo

inline > tag style > tag link

#### Especificidade

É um cálculo matemático, onde cada tipo de seletor e origem do estilo, possuem valores a serem considerados.

0. Universal selector, combinators e negation pseudo-class (:not()) = força de 0

1. Element type selectior e pseudo-elements (::before, :: after) = força de 1

10. Classes e attribute `selectors{[type="radio"]}` = força de 10

100. ID selector = força de 100

1000. Inline = o mais forte 

### Regra `!important`

* evitar o uso
* não é considerado uma boa prática
* quebra o fluxo natural da cascata
* sobrescreve qualquer regra de força

### At Rules

* Está relacionado ao comportamento do CSS
* Começa com o sinal de `@` seguido de identificador e valor

#### Exemplos comuns

- @import = incluir um CSS externo

- @media = regras condicionais para dispositivos

- @font-face = fontes externas

- @keyframes = animation

```css

@import url("http://local.com/style.css")

@media (min-width: 500px) {
  /* rules here */
}

@font-face {
  /* rules here */
}

@ekeyframes nameanimation{
  /* rules here */
}
```

### Shorthand

* junção de propriedades
* resumido
* legível

````css

/* background properties */
background-color: #00000;
background-image: url(images/image1.png);
background-repeat: no-repeat;
background-positon: left top;

/* background shortland */
background: #00000 url(images/images1.png) no-repeat left top;

/* font properties */
font-style: italic;
font-weight: bold;
font-size: .8em;
line-height: 1.2;
font-family: Aryal, sans-serif;

/* font shortland */
font: italic bold .8em/1.2 Arial, sans-serif;

````

#### Detalhes

* não irá considerar propriedades anteriores
* valores não especificados irão assumir o valor padrão
* geralmente a ordem descrita não importa, mas, se houver muitas propriedades com valores semelhantes, poderemos encontrar problemas

### Funções

* nome seguido de abre e fecha de parentêses

* recebe argumentos

````css 
@import url("http://urlaqui.com/style.css);

{
  color: rgb(255, 0, 100);
  width: calc(100% - 10px);
}
````

### Vendor Prefixes

* Permite que browsers adicione `features` a fim de colocar em uso alguma novidade que temos no CSS

* webkit = chrome, safari, ios e android
* moz = mozilla (firefox)
* ms = internet explorer
* o = opera