Pegando elementos com a DOM
```js
const h1 = document.querySelector('h1')
const links = document.querySelectorAll('a') //NodeList
```

Alterar texto com a DOM
```js
h1.innerText = "Alo"
```

Alterando estilos com a DOM
```js
h1.classList.add("hide")
h1.classList.remove("hide")
h1.style.backgroundColor = "red"
```