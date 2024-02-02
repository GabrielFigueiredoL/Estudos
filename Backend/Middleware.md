Função que tem aceso ao objeto de solicitação ([[Requisições]]), o objeto de resposta (resposta), e a próxima função de middleware no ciclo solicitação-resposta do aplicativo.

A próxima função middleware é comumente denotada por uma variável chamada next.

Middleware pode:
- Executar qualquer código
- Fazer mudanças nos objetos de solicitação e reposta
- Encerrar o ciclo de solicitação-resposta
- Chamar o próximo middleware na pilha

É possível fazer middlewares para [[Autorização]], [[Autenticação]] ou qualquer outra função necessária.