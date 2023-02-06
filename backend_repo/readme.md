### - Instalando as dependencias:

Faça o clone na sua maquina e rode o comando `yarn`

### - Inicializando:

Configure o seu .env , rode o comando `yarn typeorm migration:run -d src/data-source.ts` e depois para inicializar a aplicacao `yarn dev`.

### - Dados esperados:

### - localhost:8000/users -- Rota de criação de cliente:

{
"username":"Zeca",
"password":"12345",
"full_name": "José Carlos",
"contacts": [{
"email": "ze@mail.com.br",
"telephone" :"99999-9999"
}]
}

Resposta Esperada -- 201 Created

{
"id": "31410c7f-5ffa-4ae6-84ef-269f74110867",
"username": "Zeca",
"full_name": "José Carlos",
"createdAt": "2023-01-06T03:24:40.330Z",
"client": [],
"contacts": [
{
"email": "ze@mail.com.br",
"telephone" :"99999-9999"
}
]
}

### - http://localhost:8000/login -- Rota para login

Rota utilizada para fazer o login e pegar o token:

Exemplo de envio:

{
"username": "Zeca",
"password": "12345"
}

Resposta Esperada: 200 - Ok

{
"token": string
}
