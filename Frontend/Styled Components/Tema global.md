## Passo a Passo

1. Criar pasta `styles` na `src` do projeto e um arquivo `theme.js`
2. exportar as cores que serão usadas
```js
export default {
	COLORS: {
	BACKGROUND_900: "#232129",
	BACKGROUND_800: "#312E38",
	BACKGROUND_700: "#3E3B47";

	WHITE: "#F4EDE8",
	ORANGE: "#FF9000",
      
	GRAY_100: "#999591",
	GRAY_300: "#666360",
      
	RED: "#FF002E"
	}
}
```

3. No arquivo `main.js` importar o `ThemeProvider` do styled-components
4. Envolver tudo no `<ThemeProvider></ThemeProvider>`
5. Adicionar a propriedade `theme` 
```js
ReactDOM.createRoot(document.getElementById('root')).render(
  <React.StrictMode>
    <ThemeProvider theme={theme}>
      <Details />
    </ThemeProvider>
  </React.StrictMode>,
)
```

## Configurações Globais

1. Criar arquivo `global.js` na pasta `styles`
2. Importar `createGlobalStyle`
```js
import { createGlobalStyle } from "styled-components";

export default createGlobalStyle`
  * {
    padding: 0;
    margin: 0;
    box-sizing: border-box;
  }

  body {
    background-color: ${({ theme }) => theme.COLORS.BACKGROUND_800};
    color: ${({ theme }) => theme.COLORS.WHITE}
  }

  a {
    text-decoration: none
  }

  

  button, a {
    cursor: pointer;
    transition: filter 0.2s;
  }
  
  button:hover, a:hover {
    filter: brightness(0.9)
  }
`
```

3. Adicionar o `GlobalStyles` no `main.js`
```js
import { ThemeProvider } from 'styled-components'
import GlobalStyles from './styles/global'
import theme from './styles/theme'

ReactDOM.createRoot(document.getElementById('root')).render(
  <React.StrictMode>
    <ThemeProvider theme={theme}>
      <GlobalStyles />
      <Details />
    </ThemeProvider>
  </React.StrictMode>,
)
```