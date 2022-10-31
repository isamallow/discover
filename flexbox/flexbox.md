# Layouts e evolução

- layout tem a ver com a maneira que os elemento estão distruibuidos na tela

## Normal flow

- ou Flow Layout é a maneira que os elementos `block` e `inline` ficam na página

```html
<p>Texto block com <strong>inline</strong> dentro</p>
```

## Tables

- é a maneira de tabelas onde a tag `table` recebe um display `table` fazendo com que os elementos internos como `td` e `tr` possam ser usados para montar uma tabela

```html
<table>
  <tr>
    <td>Hora</td>
    <td>20:00</td>
  </tr>
  <tr>
      <td>Hora</td>
      <td>20:13</td>
  </tr>
 </table>
```

## Tabless

* uso das propriedades `float`, `clear` para que os elementos possam mudar de posição na tela

```html
<div style="float: left">
esquerda
</div>
<div style="float: right">
direita
</div>
<div style="clear: both">
normal
</div>
```

## Flexbox

* a caixa se torna flex, fazendo que os elementos internados possam receber melhor:

- alinhamento
- ordenação
- tamanhos flexíveis

### Terminologia

- Flex Container (uma caixa que tem elementos dentro)
  - Flex item (dentro do flex container)
- Nesting (elementos vivem dentro de outros elementos)
- Axis (eixo principal e cruzado)
  - main (principal)
    - start, end
  - cross (cruzado)
    - start, end
- Flex sizing 
  - flexível
  - altera width/height dos itens para preenchimento dos espaços do flex container

### Propriedades do FLex Container

* direção dos itens
* multi linhas
* alinhamento
  * principal
  * cruzado
* espaços entre os itens

#### Direção dos items

* flex é uma dimensão (horizontal ou vertical)
* podemos mudar a direção com `flex-direction`
* valores: row | row-reverse| column | column-reverse

#### flex-wrap

* podemos utilizar multi linhas
* cada nova linha, um novo flex container

#### flex-flow

* shorthand
* flex-direction || flex-wrap

```css
.box {
  display: flex;
  flex-flow: column wrap;
}
```

#### justify-content

* alinhamento dos itens dos elementos dentro do container
* distribuição dos elementos

##### valores

- flex-start (padrão)
- flex-end (agrupados no final)
- center (agrupados no centro)
- space-around (agrupados com espaços ao redor dos elementos)
- space-between (agrupados com espaços ENTRE eles)
- space-evenly (espaço por igual entre os elementos)

#### align-items

* alinhamento dos elementos no eixo cruzado

##### valores

- stretch (esticados no eixo cruzado) = padrão
- flex-start (início do eixo cruzado)
- flex-end (fim do eixo cruzado)
- center (centro do eixo cruzado)

#### gap

* espaços entre os elementos

##### valores

- unidades de medidas
- fixas: px, pt
- flexíveis: %, em, rem

### Propriedades para os itens

- flex-basis
- flex-grow
- flex-shrink
- flex
- order

##### flex-grow

* o crescimento do item dentro do container em relação aos espaços vazios

##### flex-shrink

* o encolher do item dentro do container 

##### flex

* shorthand
* flex-grow | flex-shrink | flex-basis
* podem ter 1, 2 ou 3 valores

`Obs: o basis tem mais força que as outras propriedades`

#### order

* ordenar os elementos dentro da caixa
* serve como maneira visual e não estrutural