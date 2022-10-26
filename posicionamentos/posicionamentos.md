## Page Layouts

- Tables
- Floats e clear
- Frameworks e Grid Systems
- Flexbox
- Grid

## Posicionamentos

* Controlar onde, na página, o elemento irá ficar, alterando o fluxo normal dos elementos.

- Name: position
- Value: static | relative | absolute | fixed

`OBS: o padrão são todos static.`

#### Relative

- top, right, bottom, left, z-index

* fluxo normal dos elementos

#### Absolute

- top, right, bottom, left, z-index

* absoluto a sua página inteira

* é possível que o position absoluto seja referente ao elemento pai

#### Fixed

* o elemento fica fixo na página

#### Element Stacking

* É o empilhamento de elementos. Podemos usar o z-index para determinar a ordem da posição do elemento. Quanto maior o z-index, mais "acima" vai aparecer o elemento.

#### Flexbox

* nos permite posicionar os elementos dentro da caixa
* controle em uma dimensão (horizontal ou vertical)
* alinhamento, direcionamento, ordenar e tamanhos

```css
div.parent {
  display: flex;
}
```

##### flex-direction

* a direção do flex: horizontal ou vertical
* row | column

##### alinhamento

* justify-content
- space-between (espaçamento entre os elementos)
- center (juntos mas ao centro)
* align-items

## Grid

* posicionamento dos elementos dentro da caixa
* posicionamento horizontal ou vertical ao mesmo tempo
* pode ser flexível ou fixo
* cria espaços para os elementos filhos habitarem

```css
body {
  margin: 0;
  height: 100vh;
  display: grid;
  grid-template-areas:

  "header header"
  "main aside"
  "footer footer";
/* 1fr = uma fração */
  grid-template-rows: 30px 1fr 40px;
  grid-template-columns: 1fr 80px;
}
```

## Grid ou Flexbox

* é possível utilizar ambos juntos