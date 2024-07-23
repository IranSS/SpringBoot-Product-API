# SpringBootProductAPI

Este projeto é uma API REST Full desenvolvida em Java 17 utilizando o framework Spring na versão 3.3.1. O objetivo deste projeto é fornecer uma estrutura robusta para operações CRUD (Create, Read, Update, Delete) com um banco de dados PostgreSQL.

## Tecnologias Utilizadas

- **Java 17**: Linguagem de programação utilizada.
- **Spring Framework 3.3.1**: Framework principal para desenvolvimento da aplicação.
- **PostgreSQL**: Banco de dados relacional utilizado para armazenar os dados.
- **Spring Boot Starter Web**: Starter do Spring Boot para construção de aplicações web, incluindo RESTful.
- **Spring Boot Starter Data JPA**: Starter do Spring Boot para integração com JPA, facilitando o acesso a dados com repositórios Spring Data.
- **Spring Boot Starter Validation**: Starter do Spring Boot para validação de dados.
- **Spring Boot Starter HATEOAS**: Starter do Spring Boot para implementar HATEOAS (Hypermedia as the Engine of Application State).

## Funcionalidades

- Operações CRUD completas para os recursos definidos.
- Validação de dados de entrada para assegurar a integridade dos dados.
- HATEOAS para tornar a API mais autodocumentada e navegável.
- Integração com PostgreSQL para persistência dos dados.

## Estrutura do Projeto

- **SpringbootApplication**: Script principal para iniciar o projeto.
- **Controllers**: Pasta que contém os controllers da aplicação.
    - **ProductController**: Script onde se encontram as operações CRUD, baseadas nos mapeamentos Post, GetOne, GetAll, Put, e Delete.

## Como Executar

1. **Pré-requisitos**:
    - JDK 17
    - PostgreSQL
    - Maven

2. **Clonar o Repositório**:
   ```bash
   git clone https://github.com/seu-usuario/nome-do-projeto.git
   cd nome-do-projeto
3. **Configurar o Banco de Dados**:
    - Crie um banco de dados no PostgreSQL.
    - Atualize as configurações no arquivo `application.properties` com as credenciais do seu banco de dados.

4. **Executar a Aplicação**:
   ```bash
   mvn spring-boot:run
5. **Acessar a API:**
    ```bash
    A aplicação estará disponível em `http://localhost:8080`.

## Atualizações Futuras

- Implementação de segurança.
- Inclusão de novos controles.
- Outras novidades serão adicionadas conforme o desenvolvimento avança.