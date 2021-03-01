# code7Test
Aplicação para criação de dividas fictícias

tecnologias utilizadas: 
NodeJS,
MongoDB

instalação:
no arquivo .env, na sessão "DATABASE", coloque o IP de seu mongoDB e a porta e crie a base de dados "codetest" em sue mongoDB
DATABASE=mongodb://IP:PORTA/codetest

utilize o comando "npm install" no terminal na pasta do projeto para poder baixar as bibliotecas utilizadas no projeto.
utilize o comando "npm start" para iniciar o projeto.

Acesse em seu navegador o localhost:5001 para utilizar a aplicação.

para buscar as dívidas de usuário basta selecionar o usuário no canto superior esquerdo e clicar em buscar.
para cadastrar uma nova dívida, basta clicar no botão verde que contém um "+"
para alterar uma dívida basta clicar na dívida na listagem de dívidas ao lado esquerdo.
para deletar uma dívida, ao entrar na tela de edição da dívida, clique em deletar.
para atualizar uma dívida, ao entrar na tela de edição da dívida, clique em salvar.

há a possibilidade de fazer todos os processos via API, os endpoints são os seguintes:

Buscar Dividas    - Metodo GET, endpoint: /api/dividas 
Cadastrar dividas - Método POST, endpoint: /api/dividas, parâmetros: motivo(String), valor(Number), data(Date no formato DD-MM-AAAA),idUser(id do usuário na api do JSONPLACEHOLDER)
Atualizar divida  - Método PUT, endpoint: /api/divida/seq, parâmetros: motivo(String), valor(Number), data(Date no formato DD-MM-AAAA)
Buscar divida ID  - Método GET, endpoint: /api/divida/seq
Buscar divida pelo id do usuário na API  - Método GET, endpoint: /api/user/id/dividas, obs: o id passado nesse endpoint deve ser o id da api do jsonplaceholder já que no banco existe um relacionamento entre o id da api e o objeto User.
Deletar divida    - Método DELETE, endpoint: /api/divida/seq

o campo "seq" citado nos endpoints é o id sequencial das dividas, você pode saber esse id pela própria api ao usar o endpoint de busca de dividas ou na interface ao entrar na edição de uma díviva(o campo seq fica na URL).
