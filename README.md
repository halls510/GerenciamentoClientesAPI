# 🧠 Projeto: API de Gerenciamento de Clientes

Este projeto implementa uma API utilizando os princípios da **Clean Architecture** com separação em camadas, MediatR, Entity Framework Core, autenticação JWT, testes automatizados e boas práticas de desenvolvimento backend em .NET 8.

---

## 🎯 Objetivo

Demonstrar arquitetura limpa, manutenível e testável para gerenciar entidades de clientes com segurança, desacoplamento e performance.

---

## 📐 Diagrama da Clean Architecture

```text
┌─────────────────────────────────────────────┐
│                 Interface (API)             │
│       Controllers, Autenticação, Swagger    │
└─────────────────────────────────────────────┘
                   ↓ depende
┌─────────────────────────────────────────────┐
│            Infraestrutura (Infrastructure)  │
│     EF Core, Repositórios, Contextos, Logs  │
└─────────────────────────────────────────────┘
                   ↓ depende
┌─────────────────────────────────────────────┐
│           Aplicação (Application)           │
│      Casos de uso, Handlers, DTOs, MediatR  │
└─────────────────────────────────────────────┘
                   ↓ depende
┌─────────────────────────────────────────────┐
│               Domínio (Domain)              │
│         Entidades e regras de negócio       │
└─────────────────────────────────────────────┘
