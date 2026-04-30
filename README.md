# 🎯 CP2 – API de Brinquedos (Spring Boot)

## 👨‍🎓 Integrantes

* Gabriel Ambrosio Saraiva – RM XXXXX
* João Victor Vendrameto – RM 563665

---

## 📌 Descrição do Projeto

Este projeto consiste no desenvolvimento de uma API REST utilizando **Spring Boot**, com persistência em banco de dados **Oracle**, para gerenciamento de brinquedos voltados ao público infantil de até 14 anos.

A aplicação permite realizar operações de **CRUD (Create, Read, Update e Delete)** através de requisições HTTP testadas via Postman.

---

## 🛠️ Tecnologias Utilizadas

* Java 17
* Spring Boot
* Spring Data JPA
* Maven
* Oracle Database
* Postman

---

## ⚙️ Configuração do Projeto

O projeto foi criado utilizando o Spring Initializr com as seguintes configurações:

* **Group:** br.com.fiap
* **Artifact:** brinquedos
* **Packaging:** Jar
* **Java:** 17

Dependências utilizadas:

* Spring Web
* Spring Data JPA
* Oracle Driver

---

## 🗄️ Estrutura do Banco de Dados

Tabela utilizada:

```sql
CREATE TABLE TDS_TB_BRINQUEDOS (
    ID NUMBER PRIMARY KEY,
    NOME VARCHAR2(100),
    TIPO VARCHAR2(50),
    CLASSIFICACAO NUMBER,
    TAMANHO VARCHAR2(50),
    PRECO NUMBER(10,2)
);
```

---

## 🔌 Configuração da Aplicação

Arquivo `application.properties`:

```properties
spring.datasource.url=jdbc:oracle:thin:@localhost:1521:XE
spring.datasource.username=SEU_USUARIO
spring.datasource.password=SUA_SENHA

spring.jpa.hibernate.ddl-auto=update
spring.jpa.show-sql=true
spring.jpa.database-platform=org.hibernate.dialect.OracleDialect

server.port=8080
```

---

## 📁 Estrutura do Projeto

```
src/main/java/br/com/fiap/brinquedos/
│
├── controller
├── service
├── repository
└── model
```

---

## 🌐 Endpoints da API

### 🔹 GET – Listar todos os brinquedos

```
GET http://localhost:8080/brinquedos
```

---

### 🔹 GET – Buscar por ID

```
GET http://localhost:8080/brinquedos/{id}
```

---

### 🔹 POST – Criar brinquedo

```
POST http://localhost:8080/brinquedos
```

📌 Exemplo de JSON:

```json
{
  "id": 1,
  "nome": "Carrinho",
  "tipo": "Veículo",
  "classificacao": 10,
  "tamanho": "Médio",
  "preco": 49.90
}
```

---

### 🔹 PUT – Atualizar brinquedo

```
PUT http://localhost:8080/brinquedos/{id}
```

---

### 🔹 DELETE – Remover brinquedo

```
DELETE http://localhost:8080/brinquedos/{id}
```

---

## 🧪 Testes

Os testes foram realizados utilizando o Postman, validando todas as operações de CRUD:

* Inserção de dados (POST)
* Consulta de dados (GET)
* Atualização (PUT)
* Exclusão (DELETE)

📸 *Inserir prints dos testes aqui*

---

## 🚀 Execução do Projeto

1. Clonar o repositório
2. Configurar o banco Oracle
3. Ajustar o `application.properties`
4. Executar a aplicação
5. Testar via Postman

---

## 📌 Observações

A aplicação está configurada com `spring.jpa.hibernate.ddl-auto=update`, permitindo a criação e atualização automática das tabelas no banco de dados sem perda de dados existentes.

---

## 📎 Repositório

Adicionar link do GitHub aqui.

---
