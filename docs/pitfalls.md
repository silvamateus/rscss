# Pitfalls(armadilhas)

## Sangramento para componentes aninhados
Seja cuidadoso com componentes aninhados com elementos compartilhando mesmo nome de elementos no container .

```html
<article class='article-link'>
 <div class='vote-box'>
    <button class='up'></button>
    <button class='down'></button>
    <span class='count'>4</span>
  </div>

  <h3 class='title'>Article title</h3>
  <p class='count'>3 votes</p>
</article>
```

```scss
.article-link {
  > .title { /* ... */ }
  > .count { /* ... (!!!) */ }
}

.vote-box {
  > .up { /* ... */ }
  > .down { /* ... */ }
  > .count { /* ... */ }
}
```

Neste caso se `.article-link > .count` não tiver o seletor (filho)`>` também aplicará ao elemento`.vote-box .count`. Essa é uma das razões que seletores filho são preferidos.
