## Descrição

O projeto consiste na criação de um sistema de transferência entre contas bancárias.

## Tecnologias e requisitos

* Back-end - Go (Sem a utilização de framework) / 2 aplicações idênticas (uma para cada banco)
* Docker para orquestar o ambiente da aplicação
* RabbitMQ ou qualquer outro sistema de mensageria
* Banco de dados MySQL / 2 bancos de dados independentes

## Contexto do sistema

Os usuários de um banco acessarão uma página na WEB que mostrará o saldo de sua conta bancária e será possível fazer
transferências de valores entre as contas deste banco. As transferências deverão ser validadas, correntistas sem saldo
ou conta inválidas deverão ser informadas ao usuário no momento da transferência.

Os usuários também poderão ver o histórico de transações de sua conta bancária.

## Design do sistema

### Back-end

Você deve criar uma API REST que aceita realizar a listagem das transações, mostrar o saldo atual e fazer transferências entre as contas.

Além disto, esta aplicação deverá criar um consumidor do RabbitMQ ou qualquer outro sistema de mensageria para fazer transferências entre as contas.

Criar a aplicação usando pirâmides de testes será muito bem vindo.

### Concorrência

Lembre-se de pensar em concorrência no processo de transferência bancária, uma vez que vários usuários podem estar realizando transferência.

Criar a aplicação usando pirâmides de testes será muito bem vindo

## Docker

Crie as duas aplicações montando-as com Docker de forma que ao fazer `docker-compose up` seja possível testar todo o ambiente. 
O Docker deve levantar os 2 back-ends, 2 banco de dados e o RabbitMQ.

## Entrega

Subir a aplicação em um repositório Git remoto e disponibilizar o link.
