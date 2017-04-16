# Variantes

Componentes podem ter variantes. Elementos podem ter variantes também.

![](images/component-modifiers.png)

<br>

## Nomeando variantes
Classnames para variantes serão prefixados por hífen (`-`).

  ```scss
  .like-button {
    &.-wide { /* ... */ }
    &.-short { /* ... */ }
    &.-disabled { /* ... */ }
  }
  ```

## Variantes de elemento
Elementos também podem ter variantes.

  ```scss
  .shopping-card {
    > .title { /* ... */ }
    > .title.-small { /* ... */ }
  }
  ```

## Dash prefixes
Hífens são prefixos preferíveis para variantes.

  * Previne ambiguidade com elementos.
  * uma classe CSS só pode iniciar com uma letra, `_` or `-`.
  * Hífens são mais fáceis de escrever do que underscores.
  * Se assemelham a switches em comandos UNIX (`gcc -O2 -Wall -emit-last`).

Como lidar com elementos complexos? Aninhe-os..
[Continue →](nested-components.md)
<!-- {p:.pull-box} -->
