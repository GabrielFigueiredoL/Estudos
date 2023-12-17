Quando utilizamos o `GET`, os parâmetros são passados no cabeçalho da requisição. A partir de [[Query Params]] e/ou [[Route Params]] o servidor recebe os dados.

As duas maneiras mudam a forma de escrever o código, veja:

```jsx
/**
* Query params = ?name=Thiago
* Route params = /users/1
*/

// Query params: ?name=thiago

// faça a requisição no navegador: http://localhost:3333/users/?name=Thiago
server.get("/users", (req, res) => {
 const name = req.query.name;	
 return res.json({ message: `Hello ${name}` });
});

// Route Params = /users/1

// faça a requisição no navegador: http://localhost:3333/users/1
server.get("/users/:id", (req, res) => {
 // const id = req.params.id; 
 const { id } = req.params; // desestruturado com ES06	
 return res.json({ message: `Buscando o usuário de ID: ${id}`});
});
```
