#### Manipulando strings

- Maiuscula e minuscula
```js
string.toLowerCase()
string.toUpperCase()
```

- Separar string - Irá virar um array
```js
string.split(" ")
```

- Verificar se existe algo na string - case sensitive
```js
string.includes("palavra")
```

#### Manipulando Array

- Transformar Array em string
```js
array.join(" ")
```

- Criar array com construtor
```js
let array = new Array(10) // array com 10 posições vazias
let array = new Array ('a', 'b', 'c') // [a, b, c]
```

- Contar elementos de um array
```js
array.length()
```

- Transformar cadeia de caracteres em um array
```js
let word = 'abc'
Array.from(word) // [a, b, c]
```

- Adicionar um item no fim
```js
array.push("item")
```

- Adicionar no começo
```js
array.unshift('item')
```

- Remover do fim
```js
array.pop()
```

- Remover do começo
```js
array.shift()
```

- Pegar somente alguns elementos do array
```js
array.slice(1, 3) // posição de inicio, posição final
```

- Remover um ou mais itens em qualquer posição do array
```js
array.splice(1, 2) //index, qntd de elementos
```

- Encontrar a posição de um elemento no array
```js
array.indexOf("item")
```