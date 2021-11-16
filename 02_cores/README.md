# Cores de texto
A aplicação ou website possuem um estilo a ser seguido, geralmente esse estilo é definido pelo _designer_ da interface. Nesse guia de estilos há fontes, tamanhos de fontes e cores que devem ser utilizadas. O Bootstrap utiliza esse esquema de cores para definir o seu sistema de cores.

## Objetivos
1. Compreender o sistema de cores do Bootstrap
2. Utilizar o recurso de opacidade.

## Roteiro
O Bootstrap disponibiliza a maior parte de seus recursos no formato de [classes](https://developer.mozilla.org/pt-BR/docs/Web/CSS/Class_selectors) no CSS e essas classes podem ser utilizadas, mais de uma por vez, para aplicar alguma formatação desejada, como o apresentarei nesse roteiro as cores e opacidade. A documentação oficial das cores fica [neste link](https://getbootstrap.com/docs/5.1/utilities/colors/).

### Cores no texto
As formatações voltadas exclusivamente para texto começam com o prefixo `text-`, é assim nas cores e será assim em outros roteiros. As cores foram pensadas em sua utilização dentro de uma interface. Há cores para o texto padrão, há cores para destacar algo, para chamar a atenção, para informar, etc. Não pensem em utilizar o Bootstrap achando que encontração algo como `text-yellow`, **isso não existe!**. A cor da fonte padrão não precisa ser formatada com nenhuma classe, o Bootstrap formata automaticamente, quando há a necessidade de sair do padrão é que devemos recorrer a uma das formatações abaixo:

![Cores](./imgs/cores.png)

Estas cores podem ser modificadas através do processo de personalização, portanto, um website pode mudar completamente suas cores sem mudar uma única linha de seu HTML, tudo o que foi marcado como cor primária, continuará como cor primária, o que mudará será essa cor.

O HTML que gerou a imagem mostrada anteriormente é este aqui:

```html
<p class="text-primary">.text-primary</p>
<p class="text-secondary">.text-secondary</p>
<p class="text-success">.text-success</p>
<p class="text-danger">.text-danger</p>
<p class="text-warning bg-dark">.text-warning</p>
<p class="text-info bg-dark">.text-info</p>
<p class="text-light bg-dark">.text-light</p>
<p class="text-dark">.text-dark</p>
<p class="text-body">.text-body</p>
<p class="text-muted">.text-muted</p>
<p class="text-white bg-dark">.text-white</p>
<p class="text-black-50">.text-black-50</p>
<p class="text-white-50 bg-dark">.text-white-50</p>
```

Observem que em alguns casos, há a utilização de mais de uma classe, é o caso em que deseja-se modificar, além da cor do texto, a cor de fundo. Como a formatação de cor de fundo não se aplica **exclusivamente** aos textos, a classe de mudança da cor de fundo começa com `bg-`.

Embora seja possível formatar links com estas mesmas classes, é recomendado que não o faça, pois há recursos próprios para formatação de links, facilitando quando a aplicação/website mudar de estilo (o que pode ocorrer de tempos em tempos).

### Opacidade
A opaco é algo que não possui transperência. Os elementos no HTML são por padrão opacos, mas em alguns casos desejamos algum nível de transparência, por exemplo uma configuração desativada. As opções de opacidade de **texto** do Bootstrap são quatro, 100% (valor padrão, que não precisa ser marcado), 75%, 50% e 25%. Quanto maior o número, menos transparência terá. Abaixo está o exemplo da aplicação de transparência em um texto que já está marcado com a cor primária.

![Opacidade](./imgs/opacidade.png)

Imagem gerada pelo HTML:
```html
<div class="text-primary">This is default primary text</div>
<div class="text-primary text-opacity-75">This is 75% opacity primary text</div>
<div class="text-primary text-opacity-50">This is 50% opacity primary text</div>
<div class="text-primary text-opacity-25">This is 25% opacity primary text</div>
```

## Atividade
1. Copie e cole alguns parágrafos de alguma notícia, marque-os como parágrafo (`<p>`).
2. Usando o `<span>` destaque alguns trechos usando alguma das cores disponíveis no Bootstrap.
3. Aplique transparência em algum trecho que não achou interessante (não esqueça de marcar esse trecho com `<span>`). Escolha qualquer das cores disponíveis para utilizar com a transparência.