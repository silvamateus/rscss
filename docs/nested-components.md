# Componentes aninhados

![](images/component-nesting.png)

```html
<div class='article-link'>
  <div class='vote-box'>
    ...
  </div>
  <h3 class='title'>...</h3>
  <p class='meta'>...</p>
</div>
```

Às vezes é necessário aninhar componentes. Aqui estão algumas diretrizes para fazer isso.

## Variantes
Um componente precisa parecer de certa forma quando aninhados em outro componente. Evite modificar o componente aninhado utilizando o componente que o contém.

```scss
.article-header {
  > .vote-box > .up { /* ✗ avoid this */ }
}
```

  Ao invés disso prefira adicionar um variante ao componente aninhado e aplique do componente que o contém.

```html
<div class='article-header'>
  <div class='vote-box -highlight'>
    ...
  </div>
  ...
</div>
```

```scss
.vote-box {
  &.-highlight > .up { /* ... */ }
}
```

## Simplificando componentes aninhados
às vezes quando aninha componentes, seu markup pode ficar sujo:

```html
<div class='search-form'>
  <input class='input' type='text'>
  <button class='search-button -red -large'></button>
</div>
```

Você pode simplificá-lo utilizando seu mecanismo de preprocessamento CSS `@extend`:

```html
<div class='search-form'>
  <input class='input' type='text'>
  <button class='submit'></button>
</div>
```

```scss
.search-form {
  > .submit {
    @extend .search-button;
    @extend .search-button.-red;
    @extend .search-button.-large;
  }
}
```

Que tal repetir elementos como em uma lista? Aprenda sobre Layouts.
[Continue →](layouts.md)
<!-- {p:.pull-box} -->
