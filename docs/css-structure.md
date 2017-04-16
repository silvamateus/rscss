# Estrutura CSS

## Um componente por arquivo
Coloque cada componente em seu próprio arquivo.

  ```scss
  /* css/components/search-form.scss */
  .search-form {
    > .button { /* ... */ }
    > .field { /* ... */ }
    > .label { /* ... */ }

    // variants
    &.-small { /* ... */ }
    &.-wide { /* ... */ }
  }
  ```

## Use glob matching
Em sass-rails e stylus, Isso torna fácil incluir todos:

  ```scss
  @import 'components/*';
  ```

## Evite over-nesting
Não use mais do que 1 nível de aninhamento. É mais fácil se perder com muito aninhamento.

  ```scss
  /* ✗ Evite: 3 níveis de aninhamento */
  .image-frame {
    > .description {
      /* ... */

      > .icon {
        /* ... */
      }
    }
  }

  /* ✓ Melhor: 2 níveis */
  .image-frame {
    > .description { /* ... */ }
    > .description > .icon { /* ... */ }
  }
  ```
