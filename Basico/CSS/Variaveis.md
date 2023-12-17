[[CSS]]

É possível utilizar para medidas, cores, etc

Para declarar um variável:
```css
:root {
	--nome-variavel: #FF21F4;
	--main-color: #F1F1F2;
	--secondary-color: #010102;
}
```

Para utilizar:
```css
element {
	color: var(--main-color)
}

.element {
	background-color: var(--secondary-color)
}
```

É possível também, utilizar cores hsl:
```css
:root {
	--primary-color: hsl(57, 100%, 36%);
	--secondary-color: hsl(57, 68%, 56%);
}
```

Como ambas as cores possuem a primeira propriedade em comum, é possível utilizar uma variável:
```css
:root {
	--main-color: 57;
	--primary-color: hsl(var(--main-color), 100%, 36%);
	--secondary-color: hsl(var(--main-color), 68%, 56%);
}
```

Logo, seria possível sair de um site com tons amarelos para um site com tons vermelhos mudando apenas uma propriedade: 
```css
:root {
	--main-color: 0;
	--primary-color: hsl(var(--main-color), 100%, 36%);
	--secondary-color: hsl(var(--main-color), 68%, 56%);
}
```

