# SpringBootProductAPI

Este projeto é uma API RestFul desenvolvida em Java 17 utilizando o framework Spring na versão 3.3.2. O objetivo deste projeto é fornecer uma estrutura robusta para operações CRUD (Create, Read, Update, Delete) com um banco de dados PostgreSQL.

## Tecnologias Utilizadas

- **Java 17**: Linguagem de programação utilizada.
- **Spring Framework 3.3.2**: Framework principal para desenvolvimento da aplicação.
- **PostgreSQL**: Banco de dados relacional utilizado para armazenar os dados.
- **Spring Boot Starter Web**: Starter do Spring Boot para construção de aplicações web, incluindo RESTful.
- **Spring Boot Starter Data JPA**: Starter do Spring Boot para integração com JPA, facilitando o acesso a dados com repositórios Spring Data.
- **Spring Boot Starter Validation**: Starter do Spring Boot para validação de dados.
- **Spring Boot Starter HATEOAS**: Starter do Spring Boot para implementar HATEOAS (Hypermedia as the Engine of Application State).
- **Spring Security 6.3.1**: Implementado para fornecer segurança básica à API.

## Funcionalidades

- Operações CRUD completas para os recursos definidos.
- Validação de dados de entrada para assegurar a integridade dos dados.
- HATEOAS para tornar a API mais autodocumentada e navegável.
- Integração com PostgreSQL para persistência dos dados.
- **Segurança**: Implementação de autenticação básica utilizando Spring Security, com dados de usuários armazenados em uma tabela no banco de dados PostgreSQL.

## Estrutura do Projeto

- **SpringbootApplication**: Script principal para iniciar o projeto.
- **controllers**: Pasta que contém os controllers da aplicação.
   - **ProductController**: Script onde se encontram as operações CRUD, baseadas nos seguintes mapeamentos:
      - **POST /products**: Salva um novo produto. Acesso restrito a usuários com o papel `ROLE_ADMIN`.
      - **GET /products**: Retorna a lista de todos os produtos, com links para detalhes de cada produto. Acesso permitido para `ROLE_ADMIN` e `ROLE_USER`.
      - **GET /products/{id}**: Retorna os detalhes de um produto específico pelo seu ID. Acesso permitido para `ROLE_ADMIN` e `ROLE_USER`.
      - **PUT /products/{id}**: Atualiza as informações de um produto existente. Acesso restrito a usuários com o papel `ROLE_ADMIN`.
      - **DELETE /products/{id}**: Exclui um produto pelo seu ID. Acesso restrito a usuários com o papel `ROLE_ADMIN`.
   - **UserController**: Script responsável por gerenciar usuários, com o seguinte endpoint:
      - **GET /user/infousers**: Retorna a lista de todos os usuários cadastrados. Acesso restrito a usuários com o papel `ROLE_ADMIN`.
- **WebSecurityConfig**: Configuração de segurança que desativa CSRF e exige autenticação para todas as requisições.
- **UserModel**: Entidade que representa a tabela de usuários no banco de dados, implementando a interface UserDetails para integração com o Spring Security.

## Como Executar

1. **Pré-requisitos**:
   - JDK 17
   - PostgreSQL
   - Maven

2. **Clonar o Repositório**:
    ```bash
    git clone https://github.com/IranSS/SpringBoot-Product-API.git
    ```

3. **Configurar o Banco de Dados**:
   - Crie um banco de dados no PostgreSQL.
   - Atualize as configurações no arquivo `application.properties` com as credenciais do seu banco de dados.

4. **Adicionar Usuários**:
   - A criação de usuários e atribuição de roles (ADMIN e USER) deve ser feita diretamente no banco de dados até que a funcionalidade de criação pela API seja implementada.

5. **Executar a Aplicação**:
    ```bash
    mvn spring-boot:run
    ```

6. **Acessar a API**:
   A aplicação estará disponível em `http://localhost:8080`.

## Atualizações Futuras

- Outras novidades serão adicionadas conforme o desenvolvimento avança.