Recebe os dados da requisição no corpo da requisição, em um objeto em JSON. Sempre utilizando no método POST da requisição.

```jsx
{ 
	"name": "Thiago", "age": 18, "email": "thiago@mail.com"
}
```

No controller você pega a requisição para salvar os dados no banco de dados.

```jsx
server.post("/users", (req, res){ 
 const { name, age, email } = req.body; 
 await connection("users").insert({ name, age, email }); 
return res.json({ id }); }
```