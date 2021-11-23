# Sistema de grid
O sistema de grid do Bootstrap é uma organização do *espaço disponível* em um esquema de 12 colunas, com o objetivo de definir quanto de espaço um determinado conteúdo poderá ocupar (dependendo inclusive do tamanho do dispositivo).

## Objetivos
1. Entender o sistema de 12 colunas
2. Compreender a utilização de colunas responsivas

## Roteiro
O sistema de 12 colunas do Bootstrap cria uma divisão de um espaço qualquer (pode ser um `container` inteiro ou uma pequena região no rodapé da página) em 12 partes iguais, aqui chamadas de colunas.

Para realizar essa divisão é necessário a utilização de linha(s), semelhante ao que se faz em uma tabela, que é composta por linhas e colunas. No Bootstrap é necessário estabelecer uma linha, representado sempre pela classe `row` e dentro desta, as colunas. Abaixo um pequeno exemplo:

```html
<div class="container">
  <div class="row">
    <div class="col-1">Coluna 01</div>
    <div class="col-1">Coluna 02</div>
    <div class="col-1">Coluna 03</div>
    <div class="col-1">Coluna 04</div>
    <div class="col-1">Coluna 05</div>
    <div class="col-1">Coluna 06</div>
    <div class="col-1">Coluna 07</div>
    <div class="col-1">Coluna 08</div>
    <div class="col-1">Coluna 09</div>
    <div class="col-1">Coluna 10</div>
    <div class="col-1">Coluna 11</div>
    <div class="col-1">Coluna 12</div>
  </div>
</div>
```

Neste exemplo há um `container` (para fazer referência ao conteúdo anterior), mas ele não é obrigatório, pois o `row`-`col` pode ser utilizado em qualquer lugar. *Sempre serão 12 colunas*, caso seja acrescentado uma décima terceira coluna, ela será jogada automaticamente para baixo das 12 já existentes. Neste ponto deve ter percebido que o número pós fixo da classe `col` possui um significado, que é a largura que essa coluna deverá ocupar nesse sistema de 12 colunas.

Caso o exemplo fosse o mostrado abaixo:

```html
<div class="container">
  <div class="row">
    <div class="col-4">Coluna 01</div>
    <div class="col-8">Coluna 02</div>
  </div>
</div>
```

A representação seria esta:



Esta é uma representação em um dispositivo móvel (foi acrescentado cor de fundo as colunas para facilitar a visualização), mas não seria diferente (proporcionalmente) em um dispositivo grande. Na imagem é possível ver que a coluna 01 ocupa 1/3 do espaço disponível e a coluna 02 ocupa os outros 2/3 do espaço disponível. A configuração de `col-4` fez com que a coluna ocupasse 4 espaços dos 12 disponíveis, o mesmo aconteceu com o `col-8` que ocupou 8 espaços. 

O que aconteceria se o código fosse levemente modificado?
```html
<div class="container">
  <div class="row">
    <div class="col-4">Coluna 01</div>
    <div class="col-9">Coluna 02</div>
  </div>
</div>
```
![Duas colunas](./imgs/2cols_mobile_sum13.png)

O resultado seria completamente diferente, pois o `col-9` extrapola o espaço que sobrou (`12-4 = 8`), não restando alternativa a não ser coloca-lo abaixo das colunas existentes.

Este comportamento é muito útil ao criar-se uma interface que deve ser responsiva, pois podemos configurar tamanhos diferentes para as colunas dependendo do tamanho do dispositivo e recorrer a este comportamento de "jogar para baixo", forçando o conteúdo a se estender na vertical (que não há limite, pois o usuário pode rolar a barra).


## Atividade