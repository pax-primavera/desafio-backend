# Desafio Desenvolvedor Web

Desenvolver uma API RESTful utilizando Java(Spring Boot) e Postgres.

## Cenário

Na nossa empresa, surgiu a necessidade de gerenciar os cadastros dos nossos clientes, separados por filial.

## Requisitos
- Uma filial teve pertencer a um estado
- Um cliente teve pertencer a uma filial
- Um cadastro do cliente, precisa conter o plano contratado por ele
- Um cadastro precisa ser único, não pode permitir duplicidade
- Ao finalizar, criar um repositório no github e mandar o link para o email <suporte.ti@paxprimavera.com.br>

### Modelos
- Estados: (ID)Código Único, Nome, UF
    - Pode ser populado automaticamente

    - Exemplo: 
        - 1, MS 
        - 2, PR
        - 3, GO

- Cidades "Filial": (ID) Código Único, Nome
    - Pode ser populado automaticamente

        - Exemplo: 
            - 1, Dourados, 1 
            - 2, Caarapo, 1
            - 3, Juti, 1
            - 3, Navirai, 1

- Planos: (ID)Código Único, Descricao, Valor Mensalidade

  - Exemplo:
    - 1, Luxo, 80.00
    - 2, Super Luxo, 120.00

- Clientes: (ID)Código Único, CNPJ/CPF, Nome, Telefone, Endereco, Data de Contrato, Data de Cadastro, Número do contrato

## Objetivo

Queremos endpoints para gerenciar os contratos feitos pelas filiais.

### API endpoints("Rotas")

- Planos

```
GET /planos 
Codes 200
```
Retorna todos os planos

```
POST /planos
Codes 201 / 400
```
Adiciona um novo plano

```
PUT /planos/{id}
Codes 200 / 400
```
Atualiza os dados do plano

```
DELETE /planos/{id}
Codes 204 / 400
```
Apagar o cadastro do plano

- Clientes

```
GET /clientes 
Codes 200
```
Retorna todos os clientes

```
GET /clientes?
Codes 200 / 404
```
Retorna os clientes de acordo com o termo passado via querystring e paginação

```
GET /clientes/{id}
Codes 200 / 404
```
Retorna os dados de um cliente

```
POST /clientes
Codes 201 / 400
```
Adiciona um novo cliente

```
PUT /clientes/{id}
Codes 200 / 400
```
Atualiza os dados do cliente

```
DELETE /clientes/{id}
Codes 204 / 400
```
Apagar o cadastro do cliente

## Avaliação

Não se preocupe em terminar todo o teste. Procure finalizar cada requisito antes de seguir para o próximo.

### Será avaliado

- Estrutura do código
- Lógica de progamação
- Clean Code
- Documentação(Exemplo: OpenApi Swagger)
- Modelagem do Bancos de Dados
- Tratamento de dados

### Diferencial

- Docker
- Testes unitários
- Testes de integração;
- Tratamento de erros

## Entrega

O candidato tem 1 semana para concluir o desafio, a partir do envio do teste.

## Dúvidas

Abra uma [issue](https://github.com/pax-primavera/desafio-tecnico-backend/issues)

Ou envie um email para: **suporte.ti@paxprimavera.com.br**

