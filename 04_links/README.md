# Links
A coloração de links do Bootstrap segue o mesmo estilo de cores de texto, com cor primária, secundárias, etc.


## Roteiro
Por serem links suas classes possuem o prefixo `link-`, possuindo o `link-primary`, `link-secondary` e todos os outros existentes no sistema de cores. A vantagem de sua utilização em detrimento do `text-` é permitir uma maior personalização (que será abordado em outro ponto deste roteiro) voltada exclusivamente para os links. As opções disponíveis são `link-primary`, `link-secondary`, `link-success`, `link-danger`, `link-warning`, `link-info`, `link-light` e `link-dark`, como mostrado na figura abaixo:

![Links](./imgs/links.png)
```html
<a href="#" class="link-primary">Primary link</a>
<a href="#" class="link-secondary">Secondary link</a>
<a href="#" class="link-success">Success link</a>
<a href="#" class="link-danger">Danger link</a>
<a href="#" class="link-warning">Warning link</a>
<a href="#" class="link-info">Info link</a>
<a href="#" class="link-light">Light link</a>
<a href="#" class="link-dark">Dark link</a>
```

Repare que o link com formatação `link-light` não está aparecendo entre o `link-info` e o `link-dark` pela formatação ser branca (mesma cor do fundo da página).

## Atividade
1. Copiar um parágrafo de uma notícia, marcar algumas palavras como link (remetendo-as para uma página que explique o que está marcado, ex: `... ataque <a href="https://pt.wikipedia.org/wiki/Hacker">hacker</a> realizado ...`). Este link deve estar formatado com alguma das classes abordadas no roteiro.