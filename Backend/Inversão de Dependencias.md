Módulos de alto nível não devem depender de módulos de baixo nível. Ambos devem depender de abstrações; Abstrações não devem depender de detalhes. Detalhes devem depender de abstrações. (MARTIN 1996)

# Resumo
Desacoplar e diminuir a dependência entre regra de negocio e infraestrutura.
Regra de negocio: logica desenvolvida para executar/entregar algo de valor para o usuario.
ex: verificar se usuario existe, verificar se email é usado
Infraestrutura: Tudo usado para fazer a entrega.

# Controlando o acoplamento
De maneira geral, será praticamente impossível criar uma aplicação onde a arquitetura seja totalmente desacoplada e abstrata, pois acoplamentos concretos sempre existirão.

## Segredo
O segredo está em saber diferenciar os acoplamentos ruins dos acoplamentos bons, pois assim “modelaremos nossos sistemas fugindo dos “acoplamentos perigosos”.

## Exemplo de acomplamento

![[Pasted image 20231223202645.png]]

![[Pasted image 20231223202929.png]]
