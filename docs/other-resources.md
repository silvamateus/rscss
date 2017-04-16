# Other resources

 * [ITCSS](https://speakerdeck.com/dafed/managing-css-projects-with-itcss#49) ("Inverted Triangle CSS") é um bom componente para qualquer rscss.
 * [rsjs](http://ricostacruz.com/rsjs/) ("Reasonable Standard of JavaScript Structure") é um documento para estruturar JavaScript em sites simples que é um trabalho-em-andamento.

Outras soluções
---------------

### BEM
[BEM] é legal, mas alguns podem ter repulsa por sua sintáxe não convencional. RSCSS segue muitas convenções BEMis, porém com sintáxe diferente.

```html
<!-- BEM -->
<form class='site-search site-search--full'>
  <input  class='site-search__field' type='text'>
  <button class='site-search__button'></button>
</form>
```

```html
<!-- rscss -->
<form class='site-search -full'>
  <input  class='field' type='text'>
  <button class='button'></button>
</form>
```

## Terminologias

Os mesmos conceitos existem de formas em outras ideologias de estruturar CSS.

| RSCSS     | BEM      | SMACSS        |
| ---       | ---      | ---           |
| Component | Block    | Module        |
| Element   | Element  | Sub-Component |
| Layout    | ?        | Layout        |
| Variant   | Modifier | Sub-Module & State |

[BEM]: http://bem.info/
[Smacss]: https://smacss.com/
