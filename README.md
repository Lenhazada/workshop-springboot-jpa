# Workshop Spring Boot + JPA

API REST desenvolvida durante o curso de Java do **Nelio Alves (DevSuperior)** com o objetivo de aplicar os principais conceitos de desenvolvimento backend utilizando **Spring Boot**, **Spring Data JPA**, **Hibernate** e bancos de dados relacionais.

O projeto simula um sistema de e-commerce contendo usuários, produtos, categorias, pedidos, itens do pedido e pagamentos.

---

## 📚 Tecnologias utilizadas

- Java
- Spring Boot
- Spring Data JPA
- Hibernate
- Maven
- H2 Database
- REST API

---

As responsabilidades são divididas em camadas:

- **Entities** → entidades do banco
- **Repositories** → acesso aos dados
- **Services** → regras de negócio
- **Resources (Controllers)** → endpoints REST
- **Config** → configuração e carga inicial de dados
- **Exceptions** → tratamento personalizado de erros

---

# Funcionalidades

- Cadastro de usuários
- Cadastro de produtos
- Cadastro de categorias
- Cadastro de pedidos
- Associação entre produtos e categorias
- Associação entre pedidos e usuários
- Registro de pagamentos
- Tratamento de exceções
- Banco H2 para testes
- Compatível com PostgreSQL

---

# Modelo de domínio

O sistema possui as seguintes entidades:

- User
- Order
- Product
- Category
- OrderItem
- Payment

Relacionamentos implementados:

- Um usuário possui vários pedidos.
- Um pedido possui vários itens.
- Um item referencia um produto.
- Um produto pode pertencer a várias categorias.
- Um pedido possui um pagamento.

---

# Endpoints

## Usuários

| Método | Endpoint |
|---------|----------|
| GET | /users |
| GET | /users/{id} |
| POST | /users |
| PUT | /users/{id} |
| DELETE | /users/{id} |

---

## Produtos

| Método | Endpoint |
|---------|----------|
| GET | /products |
| GET | /products/{id} |

---

## Categorias

| Método | Endpoint |
|---------|----------|
| GET | /categories |
| GET | /categories/{id} |

---

## Pedidos

| Método | Endpoint |
|---------|----------|
| GET | /orders |
| GET | /orders/{id} |

---

# Banco de dados

O projeto utiliza dois bancos:

### H2

Utilizado para desenvolvimento e testes.

Console:

```
http://localhost:8080/h2-console
```

---

### PostgreSQL

O projeto também possui dependência para PostgreSQL, permitindo utilizar um banco relacional em ambiente de produção.

---

# Como executar

## Pré-requisitos

- Java
- Maven
- Git

---

### Clone o projeto

```bash
git clone https://github.com/seu-usuario/workshop-springboot-jpa.git
```

Entre na pasta

```bash
cd workshop-springboot-jpa
```

Execute

```bash
./mvnw spring-boot:run
```

ou

```bash
mvn spring-boot:run
```

A aplicação iniciará em

```
http://localhost:8080
```

---

# Exemplos de requisição

Buscar usuários

```
GET /users
```

Buscar um produto

```
GET /products/1
```

Cadastrar usuário

```
POST /users
```

```json
{
    "name": "Maria",
    "email": "maria@email.com",
    "phone": "999999999",
    "password": "123456"
}
```

---

# Tratamento de exceções

O projeto possui tratamento global de erros através de:

- ResourceExceptionHandler
- ResourceNotFoundException
- StandardError

Isso permite retornar respostas HTTP padronizadas para recursos inexistentes e outros erros da aplicação.

---

# Aprendizados

Durante o desenvolvimento deste projeto foram praticados conceitos como:

- Arquitetura em camadas
- API REST
- CRUD
- JPA/Hibernate
- Relacionamentos entre entidades
- Chaves compostas
- Enumerações
- Tratamento de exceções
- Injeção de dependências
- Configuração de perfis
- Banco H2
- Persistência de dados

---

# Melhorias futuras

- Implementar autenticação com JWT
- Documentação com Swagger/OpenAPI
- Paginação
- Validação com Bean Validation
- Docker
- Testes automatizados
- Deploy em nuvem

---

# Autor

Projeto desenvolvido durante o curso de Java do **Nelio Alves (DevSuperior)**.

Adaptado e estudado por **Gabriel Lenhardt**.
