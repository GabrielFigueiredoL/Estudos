[[CSS]]

`margin-inline`: Margem horizontal
`margin-block`: Margem vertical

`flex: 1`: O elemento ocupará todo espaço disponível 

`clamp(min, ideal, max)`: Faz algo crescer de acordo com variáveis. O valor ideal não pode ser maior nem menor que o min max.
```css
elemento {
	width: clamp(20rem, 30vw, 70rem)
}
```

 `object-fit`:  especifica como o conteúdo de um elemento substituído deve ser ajustado à caixa estabelecida pela altura e largura usadas.
 ```css
object-fit: fill
object-fit: contain
object-fit: cover
object-fit: none
object-fit: scale-down
```

`transition`:  Permite a transição entre dois estados de um elemento. É possível definir esses estados com pseudo-classes, `:hover` ou `:active` ou por meio de javascript

`filter`: Aplica efeitos visuais como contraste ou desfoque

`animation`: permite que um elemento mude gradualmente de um estilo para outro.
animista.net
```css
@keyframes nome-da-animacao {
	/*0%*/
	from {
		background-color: red;
	}
	/*100%*/  
	to {
		background-color: yellow;
	}
}  
  
/* The element to apply the animation to */  
div {  
	width: 100px;  
	 height: 100px;  
	 background-color: red;  
	 animation-name: nome-da-animacao;  
	 animation-duration: 4s;
}
```

sr-only
### Botão aparecer quando algo da caixa receber foco
```html
<div>
	<input type="text" />
	<footer>
		<button type="submit">Concluir</button>
	</footer>
</div>
```
```css
footer {
	visibility: hidden;
	max-height: 0;
}

div:focus-within footer {
	visibility: visible;
	max-height: none;
}
```

[[JavaScript]]

- Colocar title quando o botão for apenas um ícone, ajuda em leitores de tela;