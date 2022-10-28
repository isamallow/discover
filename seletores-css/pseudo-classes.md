# Pseudo-classes

* É um tipo de seletor que irá selecionar um elemento que estiver em um estado específico.

* Exemplo: É o primeiro elemento dentro de uma caixa, ou, o elemento está com o ponteiro do mouse em cima dele.

* Pseudo-classes começam com 2 pontos seguidos do nome da pseudo class `:pseudo-class-name`.

## Selecionando elementos com pseudo-classes

* :first-child (primeiro filho de um grupo de elementos)

```css 
ul li:first-child 
```
* nth-of-type()

```css 
article p:nth-of-type(1)
```

* :nth-child() (leva em consideração os filhos do elemento principal)

```css 
article p:nth-child()
```

* even (números pares)

`:nth-child(even)`

* odd (números impares)

`:nth-child(odd)`

## Ações do usuário

* :hover (o mouse em cima)
* :focus (campos de input)

## Atributos

* :disabled (desabilitado)
* :required (obrigatório)

## Referências

https://developer.mozilla.org/en-US/docs/Web/CSS/Pseudo-classes