# Flexbox
O [flexbox](https://developer.mozilla.org/pt-BR/docs/Web/CSS/CSS_Flexible_Box_Layout/Basic_Concepts_of_Flexbox) é um recurso apresentado no CSS3 e que solucionou a maioria dos problemas de disposição de elementos em uma página HTML. O Bootstrap é anterior a este recurso e se modernizou, alterando seus códigos para fazer uso do flexbox internamente, além de oferecer alguns recursos já prontos para quem deseja fugir do [sistema de grid](../09_align_sort/README.md).

## Objetivos
1. Conhecer as classes responsivas do flexbox disponíveis no Bootstrap.

## Roteiro
Para utilizar o flexbox é necessário habilitar o recurso através da classe `d-flex` (o flexbox será habilitado dentro do elemento) e o `d-inline-flex` que faz o mesmo que o anterior, mas o bloco passará a se comportar como os elementos de texto. Perceba a diferença abaixo.

![`d-flex`](./imgs/d-flex.png)
```html
<div class="d-flex p-2 bd-highlight">I'm a flexbox container!</div>
```

![`d-flex`](./imgs/d-inline-flex.png)
```html
<div class="d-inline-flex p-2 bd-highlight">I'm an inline flexbox container!</div>
```

Dentro de ambos todos os recursos do flexbox estará disponível, mas o `d-inline-flex` altera o tamanho do elemento para que ele passe a ter a largura do conteúdo, já o `d-flex` mantém o elemento ocupando 100% do espaço disponível.

Há também as variações `d-sm-flex`, `d-md-flex`, `d-lg-flex`, `d-xl-flex`, `d-xxl-flex`, `d-sm-inline-flex`, `d-md-inline-flex`, `d-lg-inline-flex`, `d-xl-inline-flex` e `d-xxl-inline-flex`.

### Direção dos elementos internos
A grande vantagem do flexbox é poder formatar a disposição dos elementos internos de acordo com a necessidade. As disposições disponíveis são em *linha* e *coluna*. Em ambas as disposições, elas podem ser invertidas.

![Flex Row](./imgs/flex-row.png)
```html
<div class="d-flex flex-row bd-highlight mb-3">
  <div class="p-2 bd-highlight">Flex item 1</div>
  <div class="p-2 bd-highlight">Flex item 2</div>
  <div class="p-2 bd-highlight">Flex item 3</div>
</div>
<div class="d-flex flex-row-reverse bd-highlight">
  <div class="p-2 bd-highlight">Flex item 1</div>
  <div class="p-2 bd-highlight">Flex item 2</div>
  <div class="p-2 bd-highlight">Flex item 3</div>
</div>
```

Os elementos internos estão sendo dispostos ao longo da linha, no primeiro exemplo a exibição é da esquerda para a direita, representado pelo `flex-row` e no segundo exemplo a ordem está invertida, implementado pelo `flex-row-reverse`.

![Flex Row](./imgs/flex-column.png)
```html
<div class="d-flex flex-column bd-highlight mb-3">
  <div class="p-2 bd-highlight">Flex item 1</div>
  <div class="p-2 bd-highlight">Flex item 2</div>
  <div class="p-2 bd-highlight">Flex item 3</div>
</div>
<div class="d-flex flex-column-reverse bd-highlight">
  <div class="p-2 bd-highlight">Flex item 1</div>
  <div class="p-2 bd-highlight">Flex item 2</div>
  <div class="p-2 bd-highlight">Flex item 3</div>
</div>
```
O mesmo pode ser feito na disposição em coluna com o `flex-column` e `flex-column-reverse`, mas neste formato os elementos internos irão ocupar 100% da largura disponível.

Nos dois casos estarão disponíveis as variações responsivas para a linha `flex-sm-row`, `flex-sm-row-reverse`, `flex-md-row`, `flex-md-row-reverse`, `flex-lg-row`, `flex-lg-row-reverse`, `flex-xl-row`, `flex-xl-row-reverse`, `flex-xxl-row`, `flex-xxl-row-reverse` e também as versões para coluna `flex-sm-column`, `flex-sm-column-reverse`, `flex-md-column`, `flex-md-column-reverse`, `flex-lg-column`, `flex-lg-column-reverse`, `flex-xl-column`, `flex-xl-column-reverse`, `flex-xxl-column` e `flex-xxl-column-reverse`.

## Alinhamento dos blocos internos
O alinhamento dos blocos internos é implementado com o [recurso de alinhamento já apresentado anteriormente](../09_align_sort/README.md#horizontal-align).

## Atividade