O teste automatizado é a utilização de ferramentas de software para automatizar um processo manual conduzido por humanos de revisão e validação da aplicação. adoção ampla do método.

## Tipos de Teste

### Teste de unidade
- Testa unidades individuais do código.
- Por exemplo, testa uma função especifica da aplicação.

### Testes de integração
- Testa as unidades do código trabalhando juntas.
- Por exemplo, testa Login que envolve uma série de etapas.

## Boas Práticas

1. Simples e rápido - Isso nos possibilita ter um feedback o mais cedo possível sobre possíveis impactos das modificações feitas no software. Além disso, facilita para podermos rodar os testes várias vezes se necessário e torna mais ágil o debug dos testes, reduzindo o tempo necessário para criar e manter os scripts.
2. Independentes - Os testes devem ser independentes entre si. Isso evita que a falha em um teste cause falha em outros testes, o que dificulta e torna bem mais demorada a investigação de problemas. O “você do futuro” vai agradecer muito ao “você do presente” por isso.
3. Ambiente - Os testes não devem depender de ambientes ou recursos externos, como serviços, API’s, banco de dados. etc. O teste deve ser capaz de rodar a qualquer momento e quantas vezes forem necessárias.


## Criando teste
jest
1. Criar arquivo básico de configuração
```js
// jest.config.js
module.exports = {
  bail: true,
  coverageProvider: "v8",

  testMatch: [
    "<rootDir>/src/**/*.spec.js"
  ],
}
```

2. Criar os testes
```js
//nomedoteste.spec.js
it("result of them sum of 2 + 2 must be 4", ()=> {
  const a = 2
  const b = 2

  const result = a + b

  expect(result).toEqual(4)
}) //(descrição objetiva, teste)
```
describe, it