Utilizado no [[CSS]] principalmente para dar propriedades especificas a certos elementos da página de acordo com o tamanho de tela do usúario.

```html
<!-- CSS media query em um elemento de link -->
<link rel="stylesheet" media="(max-width: 800px)" href="example.css" />
```

```css
/* CSS media query dentro de um stylesheet */
@media (max-width: 600px) {
  .div {
    display: none;
  }
}
```