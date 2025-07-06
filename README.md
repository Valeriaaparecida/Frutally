# 🧃 Projeto: Banco de Dados Relacional da Frutally

Este projeto foi desenvolvido como parte dos estudos nos cursos da **Alura**, utilizando o **SQL Server Management Studio (SSMS)**.  
Ele simula a estrutura de dados de uma empresa fictícia chamada **Frutally**, especializada na venda de sucos e produtos naturais.

---

## 🧩 Contexto: Necessidades da Frutally

No início, a **Frutally** mantinha as informações dos produtos e das vendas registradas em **planilhas** e até em **anotações de papel**.  
Mas, à medida que a empresa cresceu, percebeu-se a necessidade de adotar uma solução mais robusta para gerenciar esses dados de forma eficiente, segura e confiável.

Por isso, decidiu-se construir um **banco de dados relacional** para armazenar informações como:

- Produtos disponíveis
- Vendas realizadas
- Pessoas vendedoras
- Pessoas funcionárias
- Informações dos clientes

👉 Imagine ter que consultar o preço de um suco específico em um caderno, ou manter um histórico de vendas de vários anos em uma planilha de Excel ou Google Sheets...  
Essas tarefas tornam-se muito mais **rápidas**, **precisas** e **escaláveis** com o uso de um **banco de dados relacional**.

---

## 🎯 Objetivo do Projeto

- Criar tabelas representando entidades da empresa (clientes, produtos, etc)
- Definir os tipos corretos para cada campo (ex: `VARCHAR`, `DATE`, `FLOAT`, etc)
- Inserir dados de exemplo nas tabelas com `INSERT INTO`
- Realizar consultas com `SELECT`, aplicar filtros e ordenações
- Compreender erros comuns e boas práticas de modelagem

---

## 🛠️ Tecnologias Utilizadas

- **SQL Server** (motor de banco de dados)
- **SQL Server Management Studio (SSMS)** (interface de gerenciamento)
- **SQL** (linguagem de consulta estruturada)

---

## 📁 Estrutura das Tabelas Criadas

### 🧍‍♀️ TABELA DE CLIENTES

| Coluna             | Tipo de dado     | Descrição                    |
|--------------------|------------------|------------------------------|
| CPF                | `CHAR(11)`       | Chave primária               |
| NOME               | `VARCHAR(150)`   | Nome do cliente              |
| RUA                | `VARCHAR(150)`   | Endereço                     |
| COMPLEMENTO        | `VARCHAR(150)`   | Complemento do endereço      |
| BAIRRO             | `VARCHAR(150)`   | Bairro                       |
| ESTADO             | `CHAR(2)`        | Sigla do estado              |
| CEP                | `CHAR(8)`        | Código postal                |
| DATA DE NASCIMENTO | `DATE`           | Data de nascimento           |
| IDADE              | `SMALLINT`       | Idade                        |
| SEXO               | `CHAR(1)`        | Gênero                       |
| LIMITE DE CREDITO  | `MONEY`          | Limite de crédito do cliente|
| VOLUME DE COMPRA   | `FLOAT`          | Volume total de compras      |
| PRIMEIRA COMPRA    | `BIT`            | 1 = Sim / 0 = Não            |

---

### 📦 TABELA DE PRODUTOS

| Coluna             | Tipo de dado     | Descrição                    |
|--------------------|------------------|------------------------------|
| CODIGO DO PRODUTO  | `VARCHAR(20)`    | Chave primária               |
| NOME DO PRODUTO    | `VARCHAR(50)`    | Nome do produto              |
| EMBALAGEM          | `VARCHAR(50)`    | Tipo de embalagem            |
| TAMANHO            | `VARCHAR(50)`    | Volume ou quantidade         |
| SABOR              | `VARCHAR(50)`    | Sabor do produto             |
| PRECO LISTA        | `FLOAT`          | Preço do produto             |

---

## 📌 Exemplos de Comandos SQL

### ✅ Inserção de dados

```sql
INSERT INTO [TABELA DE CLIENTES]
VALUES (
  '00384393431','João da Silva','Rua Projetada A','Numero 233','Copacabana',
  'RJ','20000000','1965-03-21',57,'M',200000,3000.30,1
);
