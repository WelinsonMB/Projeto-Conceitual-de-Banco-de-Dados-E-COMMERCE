# Projeto Conceitual de Banco de Dados - E-COMMERCE

Este repositório contém a entrega do desafio de projeto do bootcamp **Heineken - Inteligência Artificial Aplicada a Dados com Copilot** da DIO. O objetivo do desafio era refinar um banco de dados desenvolvido durante as aulas, acrescentando três novas funcionalidades: 

- **Cliente PJ e PF**: Uma conta pode ser PJ (Pessoa Jurídica) ou PF (Pessoa Física), mas não pode ter as duas informações ao mesmo tempo.
- **Pagamento**: O cliente pode cadastrar mais de uma forma de pagamento.
- **Entrega**: A entrega deve ter um status e código de rastreio.

## Como resolvi o desafio

### 1. Cliente PJ e PF
Para resolver essa questão, criei duas novas entidades chamadas **Pessoa Física** e **Pessoa Jurídica**. Ambas as entidades compartilham a **PK** (chave primária) e a **FK** (chave estrangeira) da entidade **Cliente**, simulando uma superclasse onde o cliente pode ser apenas uma das duas opções (PJ ou PF), sem a possibilidade de ter ambas as informações ao mesmo tempo.

### 2. Pagamento
Para o segundo objetivo, criei uma entidade chamada **Pagamento**. Esta entidade se relaciona tanto com a entidade **Pedido** quanto com a **Cliente**. Com isso, um cliente pode ter várias formas de pagamento (1:N), e um pedido associara apenas uma forma de pagamento, e também cada forma de pagamento será exclusiva de um único cliente. Dessa forma, o cliente pode ter diversos cartões, mas um cartão pertence a apenas um cliente.

### 3. Entrega
No terceiro objetivo, criei uma entidade chamada **Entrega**, que se relaciona com a entidade **Pedido**. Cada entrega pode estar associada a apenas um pedido, e um pedido pode ter apenas uma entrega. Além disso, a entidade **Entrega** contém informações como status e código de rastreio para cada envio.

