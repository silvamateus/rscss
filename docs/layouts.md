# Layouts

![](images/layouts.png)

## Evite propriedades de posicionamento
Componentes devem ser criados de forma a serem reutilizados em contextos diferentes. Evite colocar essas propriedades em componentes:

  * Posicionamento (`position`, `top`, `left`, `right`, `bottom`)
  * Flutuantes (`float`, `clear`)
  * Margens (`margin`)
  * Dimensões (`width`, `height`) *

## Dimensões Fixas

Exceções a isso seriam elementos que tem largura/altura fixos, como avatares e logos.

## Defina posicionamento em elementos pais

Se você precisa definir, tente definí-los no contexto que eles estarão. Neste exemplo abaixo note que os widths e floats são aplicados no componente *list*, não no próprio componente.

  ```css
  .article-list {
    & {
      @include clearfix;
    }

    > .article-card {
      width: 33.3%;
      float: left;
    }
  }

  .article-card {
    & { /* ... */ }
    > .image { /* ... */ }
    > .title { /* ... */ }
    > .category { /* ... */ }
  }
  ```

Como aplicar margens fora do layout? Tente com Helpers.
[Continue →](helpers.md)
<!-- {p:.pull-box} -->
