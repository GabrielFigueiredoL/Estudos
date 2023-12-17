Recebe os dados da requisição como parâmetro na URL.
Pode conter um ou mais parâmetros, sendo eles opcionais.

Exemplos:
```js
http://minhaapi.com/banks?name=nubank
```

No exemplo acima acesso o recurso (ou rota) _banks_, filtrando por _name_. Para inserir parâmetros coloco `?` após a rota e adiciono a propriedade e valor: `name=nubank`.

```js
http://minhaapi.com/movies?name=transformers&actors=megan,peter
```

No exemplo acima acesso API de filmes, pesquisando por _name_ e _actors_. Sempre que for passar mais de um parâmetro podemos colocar `&` para separar os parâmetros.