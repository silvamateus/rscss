# Helpers

Para classes de uso geral destinadas a sobrescrever valores, coloque-as num arquivo separado e nomeie-as iniciando com underscore. São coisas etiquetadas com *!important*. Use com *muita* moderação.

```css
._unmargin { margin: 0 !important; }
._center { text-align: center !important; }
._pull-left { float: left !important; }
._pull-right { float: right !important; }
```

## Nomeando helpers
inicie nomes de classes com underscore. Isso tornatá fácil a diferenciação entre eles e modificadores definidos no componente. Underscodes também parecem um pouco feios, o que é um efeito colateral intencional: o uso de muitos helpers deve ser desencorajad.

  ```html
  <div class='order-graphs -slim _unmargin'>
  </div>
  ```

## Organizando helpers
Coloque todos os helpers em um arquivo chamado `helpers`. Place all helpers in one file called `helpers`. Embora você possa serpará-los em muitos arquivos, é preferível que mantenha o número de helpers o mínimo possível.
