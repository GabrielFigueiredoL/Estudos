#### Função anônima
```js
const sum = function(n1, n2){
	return n1 + n2
}
```

Cuidado: Depois de rodar uma função com return, a variavel retornada pode ser vista fora do escopo caso não seja let, const.
```js
const sum = function(n1, n2){
	total = n1 + n2
	return total
}

sum(7, 14)
console.log(total)
```

O total agora será visível no escopo ou acabar alterando outros valores, podendo causar problemas.

#### Arrow Function
```js
const sum = (n1, n2) => {
	return n1 + n2
}
```

#### Callback Function
```js
function sayMyName(name) {
	console.log('antes de executar a função callback')
	name()
	console.log('depois de executar a função callback')
}

sayMyName(
	() => {
		console.log('estou em uma callback')
	}
)
```

#### Função construtora
```js
function Person(name) {
	this.name = name
}

const gabriel = new Person("Gabriel")
```

- Expressão new
- Criar/instanciar um novo objeto
- this keyword

```js
função['function']()
```


