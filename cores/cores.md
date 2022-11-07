# Cores

* Usamos CSS para alterar cores do nosso documento.

## Tipos

* background-color (para caixas)
* color (para textos)
* border-color (para caixas)

## Valores

* Podemos definir os valores por:
    - palavra-chave(blue, transparent)
    - hexadecimal (#008972)
    - funções: rgb, rgba, hsl, hsla

```css
element {
  /* Keyword values */
  color: currentcolor; /* cor atual */
  
  /* <named-color> values */
  color: red;
  color: orange;
  color: tan;
  color: rebeccapurple;

  /* <hex-color> values 0-F */

  color: #090;
  color: #008800;
  color: #090a;
  color: #090900aa;

/* <rgb()> values */

color: rgb(34, 12, 64, 0.6); /* 0 - 255 */
color: rgba(34, 12, 64, 0.6);
color: rgb(34 12 64 /0.6);
color: rgba(34 12 64 / 0.3);
color: rgb(34.0 12 64 / 60%);
color: rgba(34.6 12 64 / 30%);

/* <hsl()> values */

color: hsl(30, 100%, 50%, 0.6); /* Hue - Saturation - Lumiance */
color: hsla(30, 100%, 50%, 0.6);
color: hsl(30 100% 50% / 0.6);
color: hsla(30 100% 50% / 0.6);
color: hsl(30.0 100% 50% / 60%);
color: hsla(30.2 100% 50% / 60%);

/* Global values = valores de herança */
color: inherit;
color: initial;
color: unset;
}
```

## Background

- Define um fundo para o nosso elemento.
- Sua área de atuação é a caixa toda.
- Por padrão, é transparente.

### Exemplos

- Usar cores sólidas
- Usar imagens
- Controlar
      * a posição das imagens
      * se elas se repetem ou não
      * o tamanho delas na caixa
- Usar cor e imagem juntas
- Usar cor gradiente

#### Background-color

* A propriedade background-color define a cor de fundo do elemento selecionado.

#### Background-image-repeat

* Para adicionar uma imagem como background podemos usar a propriedade background-image
* Por padrão a imagem vai se repetir e podemos modificar essa opção usando a propriedade background-repeat

```css
/* Values */
element {
background-repeat: repeat-x;
background-repeat: repeat-y;
background-repeat: repeat;
background-repeat: space;
background-repeat: round;
background-repeat: no-repeat;

/* Podedmos usar 2 valores: horizontal | vertical */
background-repeat: repeat space;
background-repeat: repeat repeat;
background-repeat: round space;
background-repeat: no-repeat round;
}
```

#### Background-position

* Com a propriedade background-position podemos mudar a posição da imagem do background.

```css

element {
  /* Pricipais valores */
background-position: top;
background-position: bottom;
background-position: left;
background-position: right;
background-position: center;
}

```

#### Background-size

* Para mudar o tamanho da imagem do background usamos a propriedade background-size.

```css

element {
  /* Values */
background-size: cover;
background-size: contain;

/* Podemos usar 2 valores, o primeiro é para a largura da imagem e o segundo é para a altura */
background-size: 40% auto;
background-size: 2em 25%;
background-size: auto 8px;
background-size: auto auto;
}

```

#### Background-origin-clip

* A propriedade `background-origin` é quem define o ponto de origem de uma imagem específica.

```css

element {
  /* Principais valores */
background-origin: border-box;
background-origin: padding-box;
background-origin: content-box;
}

```

* O `background-clip`
define se a cor ou imagem do background iniciam debaixo de sua área de borda, preenchimento ou conteúdo.

```css

element {
  /* Principais valores */
background-clip: border-box;
background-clip: padding-box;
background-clip: content-box;
background-clip: text;
}

```

#### Background-attachment

* A propriedade background-attachment determina se a posição da imagem vai ser fixa ou se vai rolar junto com o conteúdo.

```css

element {
  /* Principais valores */
background-attachment: scroll;
background-attachment: fixed;
background-attachment: local;
}

```

#### Shorthand

* Podemos usar o shorthand background para definir todos os valores do background.

```css

element {
  background: rgb() url() no-repeat right top / 50px border-box scroll;
}

```

#### Gradient

* `linear-gradient()` é a função usada para criar gradient linear com o CSS.

```css

element {
  background: linear-gradient(45deg, red, yellow);
}

```
* `radial-gradient()` é a função usada para criar gradient circular.

```css

element {
  background: radial-gradient(green, red, yellow);
  background: radial-gradient(rgba(255, 255, 255, 0), rgba(255, 0, 0, 0.2))
}

```

#### Múltiplos valores

* Podemos aplicar múltiplos backgrounds em um mesmo elemento, podendo ter cor sólida, gradiente ou imagem. Para isso basta separar por vírgula cada background.