# Valores e unidades de medida

* cada propriedade possui valores `property: value`
* estudo constante a fim de entender as propriedades e seus valores

## Prática

* como conhecer e estudar os valores na documentação?
    * `<color> <lenght>`
* os termos podem variar `values` ou `data types`

## Tipos numéricos

* `<integer>`      Número inteiro como - 10 ou 223.
* `<number>`       Número decimal como -2.4, 64 ou 0.234.
* `<dimension>`    É um `<number>` com uma unidade junto: 90 deg, 2s, 8px.
* `<percentagem>`  Representa uma fração de outro número: 50%.

### Unidades comuns

* `<lenght>`    Representa um valor de distância: px, em, vw.
* `<angle>`     Representa um ângulo: deg, rad, turn.
* `<time>`      Representa um tempo: s, ms. 
* `<resolution>`Representa resoluções para dispositivos: dpi.

## Distâncias absolutas <lenght>

* São fixas e não alteram seu valor.

Unidade   |     Nome           |  Equivalência
----------|--------------------|----------------------
cm        |   centímetros      | 1cm = 96px/2.54  
in        |   inches(polegadas)| 1in = 2.54cm = 96px  
px        |   pixels           | 1px = 1/96th of lin

* o mais comum e mais utilizado é o `px`
* não recomendado usar cm

## Distâncias relativas

* São relativas a um outro valor, pode ser elemento pai, ou root, ou o tamanho da tela.

* Benefício: Maior adaptação aos diferentes tipos de tela.

Unidade   |   Relativo a
----------|----------------------------------------------- 
em        |   Tamanho da font do pai.
rem       |   Tamanho da font do elemento raiz (root/html)
vw        |   1% da viewpor width.
vh        |   1% da viewpor height.

## Porcentagens

* Em muitos casos é tratado da mesma maneira que as distâncias `<lenght>`.
* Sempre será relativo a algum valor.

## Posições

* `<position>`
* representa um conjunto de coordenadas 2D 
    - top, right, bottom, left e center
* usado para alguns tipos de propriedades
* não confundir com a propriedade `position`

## Funções 

* Em programação, funções são reconhecidas por causar um reaproveitamento de código.

* Exemplos de funções do CSS:

    - rgb()
    - hsl()
    - url()
    - calc()

`Obs: entro dos parêntesis são passados argumentos.`

## Strings e identificadores

* Strings: texto envolto em aspas.

```css
.box::after {
	content: "Isso é uma string"
}
```

* Identificadores: podemos ter nomes de cores como red, black, gold.