# DeliveryFood - Sistema de Delivery de Refeições

## Arquitetura

Este projeto segue os princípios da Clean Architecture e Domain-Driven Design (DDD), organizado em um monolito distribuído com arquitetura modular.

### Estrutura do Projeto

```
src/
├── Api/
│   └── DeliveryFood.API/
└── Modules/
    ├── DeliveryFood.Module.Administrative/
    │   ├── Application/
    │   ├── Domain/
    │   ├── Infrastructure/
    │   └── IntegrationEvents/
    └── DeliveryFood.Module.Account/
        ├── Application/
        ├── Domain/
        ├── Infrastructure/
        └── IntegrationEvents/
```

### Camadas do Módulo

1. **Application**
   - Casos de uso da aplicação
   - Comandos e Consultas (CQRS)
   - DTOs e Mapeamentos
   - Validações

2. **Domain**
   - Regras de negócio
   - Entidades
   - Objetos de Valor
   - Eventos de domínio
   - Interfaces de repositório

3. **Infrastructure**
   - Implementações concretas
   - Persistência de dados
   - Serviços externos
   - Configurações

4. **IntegrationEvents**
   - Eventos de integração entre módulos
   - Message broker
   - Comunicação entre contextos

### Módulos do Sistema

1. **Módulo Administrativo**
   - Gestão de usuários
   - Autenticação e autorização
   - Gestão de clientes
   - Gestão de pacotes
   - Gestão de contratos
   - Gestão de cardápios
   - Gestão de pedidos

2. **Módulo de Conta**
   - Registro de usuários
   - Login e autenticação
   - Recuperação de senha
   - Gerenciamento de perfil
   - Configurações de conta
   - Histórico de atividades

## Tecnologias

- Backend: .NET 8
- Frontend: Angular
- Banco de Dados: PostgreSQL
- ORM: Entity Framework Core
- Autenticação: JWT
- Documentação da API: Swagger

## Estrutura de Pastas do Módulo

Cada módulo segue a mesma estrutura de camadas:

```
Module/
├── Application/
│   ├── Commands/
│   ├── Queries/
│   ├── Handlers/
│   └── DTOs/
├── Domain/
│   ├── Entities/
│   ├── ValueObjects/
│   ├── Events/
│   ├── Repositories/
│   └── Services/
├── Infrastructure/
│   ├── Persistence/
│   ├── Services/
│   └── Configurations/
└── IntegrationEvents/
    ├── Events/
    └── Handlers/
```

## Como Executar

1. Clone o repositório
2. Configure o banco de dados PostgreSQL
3. Execute as migrações
4. Inicie a API
5. Inicie o frontend Angular
