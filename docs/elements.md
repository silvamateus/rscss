# Elementos

Elementos são coisas dentro do seu componente.

![](images/component-elements.png)

## Nomeando elementos
Cada componente deve ter elementos. Eles devem ter classes de apenas **uma palavra**.

```scss
.search-form {
  > .field { /* ... */ }
  > .action { /* ... */ }
}
```

## Seletores de Elemento
Prefira usar o seletor filho `>` sempre que possível. Isso evita sangramento para elementos aninhados e tem melhor performance que seletores descendentes.

```scss
.article-card {
  .title     { /* okay */ }
  > .author  { /* ✓ better */ }
}
```

## Em múltiplas palavras
Para essas que precisam de duas ou mais palavras, concatene-as sem hífens ou underscores.

```scss
.profile-box {
  > .firstname { /* ... */ }
  > .lastname { /* ... */ }
  > .avatar { /* ... */ }
}
```

## Evite seletores tag
Use classnames sempre que possível. Seletores Tag são bons, mas eles podem apresentar uma pequena penalidade de performance e podem não ser tão descritivos.

```scss
.article-card {
  > h3    { /* ✗ avoid */ }
  > .name { /* ✓ better */ }
}
```

Nem todos os elementos devem parecer iguais. Variantes podem ajudar.
[Continue →](variants.md)
<!-- {p:.pull-box} -->
