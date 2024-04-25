# PicPay Simplificado - Desafio Backend

Este é um projeto de exemplo para o desafio técnico do PicPay Simplificado, uma plataforma de pagamentos simplificada. O projeto é uma aplicação backend que permite depósitos e transferências de dinheiro entre usuários e lojistas.

## Tecnologias Utilizadas

- Java
- Spring Boot
- Spring Data JPA
- H2 Database
- Lombok

## Requisitos do Projeto

- Cadastro de usuários (comuns e lojistas) com dados únicos (CPF/CNPJ e e-mail)
- Transferências de dinheiro entre usuários e para lojistas
- Validação de saldo antes da transferência
- Consulta a um serviço autorizador externo antes de finalizar a transferência
- Envio de notificação (e-mail/sms) no recebimento de pagamentos, com simulação de serviço de terceiros

## Estrutura do Projeto

O projeto está estruturado da seguinte forma:

- `src/main/java/com/example/picpaysimplificado`: Contém os pacotes Java do projeto
  - `controller`: Controladores REST para gerenciar as requisições HTTP
  - `service`: Serviços para implementar a lógica de negócio
  - `repository`: Repositórios Spring Data JPA para acesso ao banco de dados
  - `model`: Entidades de dados (usuários, transferências)
  - `util`: Classes utilitárias

## Executando o Projeto

Certifique-se de ter o Java e o Maven instalados. Para executar a aplicação:

1. Clone o repositório para sua máquina local:

   ```bash
   git clone https://github.com/seu-usuario/picpay-simplificado.git

   Navegue até o diretório do projeto:
  ```bash

cd picpay-simplificado
Execute a aplicação usando Maven:
  ```bash

mvn spring-boot:run
A aplicação estará disponível em http://localhost:8080.

Endpoints
Transferência de Dinheiro
Envie uma requisição POST para o endpoint /transfer com o seguinte corpo:

json
<code>
{
  "value": 100.0,
  "payer": 4,
  "payee": 15
}

</code>
value: Valor da transferência
payer: ID do usuário que está realizando o pagamento
payee: ID do usuário ou lojista que irá receber o pagamento
Testes
O projeto inclui testes unitários para os serviços de transferência. Para executar os testes:

```bash

mvn test
Melhorias Futuras
Implementar autenticação e segurança para proteger as operações
Adicionar documentação Swagger para documentar os endpoints
Configurar o projeto para uso de Docker e Docker Compose
