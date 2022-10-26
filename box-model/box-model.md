# Box Model

* fundamental para fazer layouts para a web
* maior facilidade para aplicar o CSS

## O que é?

* uma caixa retangular
* essa caixa possui propriedades de uma caixa 2D

- tamanho ( largura x altura) = width | height
- conteúdo = content
- bordas = border
- preenchimento interno = padding
- espaços fora da caixa = margin

* cada elemento na sua página, será considerado uma caixa

## box-sizing

* como será calculado o tamanho total da caixa?

- content-box | border-box

```css
div {
  box-sizing: border-box;
}
```

## display-block-inline

* como as caixas se comportam em relação a outras caixas
* comportamento externo das caixas

#### block

* ocupa toda a linha, colocando o próximo elemento abaixo desse
* width e height são respeitados
* padding, margin, border irão funcionar normalmente

```html
<p> <div> <section> <h1><h2><h3><h4><h5><h6>
```

#### inline

* elemento ao lado do outro
* não empurra os elementos para baixo
* width e height não funcionam
* somente valores horizontais de margin, padding e border

```html
<a> <strong> <span> <em>
```

## margin

* espaços entre elementos
* margin-top | margin-right | margin-bottom | margin-left
* values <lenght> | <percentage> | auto

```css
div {
  /* shorthand */
  margin: 12px 16px 10px 4px;
  /* top | right e left | bottom */
  margin: 12px 16px 0;
  /* top e bottom | right e left */
  margin: 8px 16px;
  /* 8px para todas as laterais */
  margin: 8px;
}
```

* obs: cuidado com margin collapsing (top se junta ao bottom)
* ocorre no display block

Exemplo:

```css
div {
  margin-bottom: 8px;
}

section {
  margin-top: 8px;
}
```

## padding

* preenchimento interno da caixa

* padding-top | padding-right | padding-bottom | padding-left
* values <lenght> | <percentage> | auto

```css
div {
  /* shorthand */
  padding: 12px 16px 10px 4px;
  /* top | right e left | bottom */
  padding: 12px 16px 0;
  /* top e bottom | right e left */
  padding: 8px 16px;
  /* 8px para todas as laterais */
  padding: 8px;
}
```

* padding poderá causar diferença na largura de um elemento

## border (e outline)

* as bordas da caixa

- value: <border-style> | <border-width> | <border-color>
- style: solid | dotted | dashed | double | groove | ridge | inset | outset
- width: <lenght>
- Color: <color>

```css
div {
  /* shorthand */
  border-top: solid 2px; /* top | right | bottom | left */

  /* style */
  border: solid;

  /* width <lenght> | style */
  border: 2px dotted;

  /* style | color */
  border: outset #f33;

  /* width | style| color */
  border: medium dashed green;
}
```

#### outline

Difere em 4 sentidos:
  - não modifica o tamanho da caixa, pois não é parte do Box Model
  - poderá ser diferente de retangular
  - não permite ajustes individuais
  - mais usado pelo user agent para acessibilidade