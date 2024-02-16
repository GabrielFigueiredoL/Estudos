```ts
interface User {
	name: string;
	bio: string;
	age: number
}

function sumAge(users: User[]) {
	let sum = 0;
	
	for (const user of users) {
		sum += user.age
	}

	return sum
}

sumAge()
```

- No lugar do parâmetro ``users: User[]`` pode ser utilizado também ``users: Array<User>``
- Agora só é possível utilizar arrays, e cada objeto dentro do array deve ter as propriedades de ``User``
- Typescript possui inferência de tipos, ou seja, não é necessário tipar toda informação. No código de exemplo, a idade é um number, o sum é um number, logo ele retornará sempre um number.
