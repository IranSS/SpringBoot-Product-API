# SpringBootProductAPI

Este projeto é uma API RestFul desenvolvida em Java 17 utilizando o framework Spring na versão 3.3.1. O objetivo deste projeto é fornecer uma estrutura robusta para operações CRUD (Create, Read, Update, Delete) com um banco de dados PostgreSQL.

## Tecnologias Utilizadas

- **Java 17**: Linguagem de programação utilizada.
- **Spring Framework 3.3.1**: Framework principal para desenvolvimento da aplicação.
- **PostgreSQL**: Banco de dados relacional utilizado para armazenar os dados.
- **Spring Boot Starter Web**: Starter do Spring Boot para construção de aplicações web, incluindo RESTful.
- **Spring Boot Starter Data JPA**: Starter do Spring Boot para integração com JPA, facilitando o acesso a dados com repositórios Spring Data.
- **Spring Boot Starter Validation**: Starter do Spring Boot para validação de dados.
- **Spring Boot Starter HATEOAS**: Starter do Spring Boot para implementar HATEOAS (Hypermedia as the Engine of Application State).
- **Spring Security**: Implementado para fornecer segurança básica à API.

## Funcionalidades

- Operações CRUD completas para os recursos definidos.
- Validação de dados de entrada para assegurar a integridade dos dados.
- HATEOAS para tornar a API mais autodocumentada e navegável.
- Integração com PostgreSQL para persistência dos dados.
- **Segurança**: Implementação de autenticação básica utilizando Spring Security, com dados de usuários armazenados em uma tabela no banco de dados PostgreSQL.

## Estrutura do Projeto

- **SpringbootApplication**: Script principal para iniciar o projeto.
- **Controllers**: Pasta que contém os controllers da aplicação.
   - **ProductController**: Script onde se encontram as operações CRUD, baseadas nos mapeamentos Post, GetOne, GetAll, Put, e Delete.
- **WebSecurityConfig**: Configuração de segurança que desativa CSRF e exige autenticação para todas as requisições.
- **UserModel**: Entidade que representa a tabela de usuários no banco de dados, implementando a interface UserDetails para integração com o Spring Security.

## Como Executar

1. **Pré-requisitos**:
   - JDK 17
   - PostgreSQL
   - Maven

2. **Clonar o Repositório**:
    ```bash
    git clone https://github.com/seu-usuario/nome-do-projeto.git
    ```

3. **Configurar o Banco de Dados**:
   - Crie um banco de dados no PostgreSQL.
   - Atualize as configurações no arquivo `application.properties` com as credenciais do seu banco de dados.

4. **Adicionar Usuários**:
   - Atualmente, os usuários precisam ser adicionados diretamente no banco de dados PostgreSQL, pois a criação de usuários por meio da API ainda será implementada.

5. **Executar a Aplicação**:
    ```bash
    mvn spring-boot:run
    ```

6. **Acessar a API**:
   A aplicação estará disponível em `http://localhost:8080`.

## Atualizações Futuras
- Inclusão de novos controles.
- Outras novidades serão adicionadas conforme o desenvolvimento avança.