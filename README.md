# Challenge ONE | Back End | Alura Forum 

### Tecnologias utilizadas:

- [IntelliJ](https://www.jetbrains.com/pt-br/idea/)
- [MySql](https://www.mysql.com/)
- [Java](https://www.java.com/pt-BR/)
- [Spring Boot](https://start.spring.io/)
- [Flyway Migration](https://start.spring.io/)
- [Spring Security](https://start.spring.io/)
- [Token JWT](https://jwt.io/)
- [Swagger](https://swagger.io/)

## Como utilizar esse repositório

- Faça um fork do projeto ou faça download pelo botão ["code"](https://github.com/FilipeRobot/challenge-alura-forum/archive/refs/heads/main.zip) do GitHub
- Tendo o projeto na sua máquina, abra-o em seu IDE preferido como Intellij ou Eclipse
- Faça o download das dependências do projeto usando o maven
- Crie um banco de dados MySQL, de preferência sem nenhuma tabela
- Defina as variáveis de ambiente
  - `DB_NAME`: O nome do banco de dados da aplicação, exemplo "db_forum_Alura_api"
  - `DB_USER`: O nome de usuário do banco de dados
  - `DB_PASSWORD`: A senha do banco de dados
  - `JWT_SECRET`: A "senha/secret" usada/o para gerar e desmontar o Token JWT
- rode o projeto

## Documentação
Esse projeto utiliza o Swagger para gerar a documentação, ao rodar o projeto você pode acessar
o EndPoint `/swagger-ui` para ver a documentação do projeto.

Nesse endpoint também é possível executar as funcionalidades da API, note que para isso a pagina vai exigir
o uso de autenticação via Token JWT que pode ser gerado através do endpoint `POST /login`, que vai exigir
um usuário previamente cadastrado no endpoint `POST /usuarios` ou na tabela `usuarios` do banco de dados do projeto.

## Endpoints - Autenticação
- `POST /login`: Faz login na aplicação, devolve o token para ser usado nas próximas requisições

## Endpoints - Usuario
- `GET /usuarios`: retorna todos os usuários
- `GET /usuarios/:id`: retorna um usuário específico
- `POST /usuarios`: cria um novo usuário com o nome, email e senha informados
- `PUT /usuarios`: atualiza os dados de um usuário específico existente
- `DELETE /usuarios/:id`: remove os dados de um usuário específico existente

## Endpoints - Cursos
- `GET /cursos`: retorna todos os cursos
- `GET /cursos/:id`: retorna um curso específico
- `POST /cursos`: cria um novo curso com o nome e categoria informados
- `PUT /cursos`: atualiza os dados de um curso específico existente
- `DELETE /cursos`: remove os dados de um curso específico existente

## Endpoints - Topicos
- `GET /topicos`: retorna todos os tópicos
- `GET /topicos/:id`: retorna um tópico específico
- `POST /topicos`: cria um novo tópico com o título, mensagem, autor e curso informados
- `PUT /topicos`: atualiza os dados de um tópico específico existente
- `DELETE /topicos`: remove os dados de um tópico específico existente

## Endpoints - Respostas
- `GET /respostas`: retorna todas as respostas
- `GET /respostas/:id`: retorna uma resposta específica
- `POST /respostas`: cria uma nova resposta com a mensagem, autor e tópico informados
- `PUT /respostas`: atualiza os dados de uma resposta específica existente
- `DELETE /respostas`: remove os dados de uma resposta específica existente