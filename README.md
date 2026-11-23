# solaris
App gestão tempo

# Solaris — Plataforma de Gestão de Tempo

> **Disciplina:** Arquiteturas de Computação em Nuvem  
  
> Equipe: Jaci Moura NEto

---

## 1. Cenário Hipotético e Problema Resolvido

**Solaris** é um aplicativo para gestão de tempo. Com o aumento de reuniões síncronas, múltiplos projetos simultâneos e alternância constante de contexto, os colaboradores enfrentavam dificuldades para:

1. Visualizar o equilíbrio real entre **foco técnico (Projeto A / Projeto B)**, **reuniões**, **estudos** e **descanso/indisponibilidade**;
2. Acompanhar a saúde dos projetos com base em **importância, prazos e volume de tarefas**;
3. Centralizar **comunicações (chat e e-mail)** e **anotações rápidas/rascunhos (notebook / sketchbook)** no mesmo fluxo de trabalho.

O **Solaris** resolve esses desafios por meio de uma aplicação web responsiva de três camadas apoiada em uma arquitetura de microsserviços conteinerizada, com alta disponibilidade e escalabilidade.
---

## 2. Estrutura do Repositório

.

├── README.md                 # Documentação técnica completa da arquitetura, HA e observabilidade

├── frontend/                 # Camada 1: Aplicação web responsiva (6 páginas) + Dockerfile

├── backend/                  # Camada 2: Microsserviços + Dockerfiles + testes

│   ├── core-time-service/    # Anéis diários, calendário e estatísticas de tempo/projetos

│   ├── comms-notes-service/  # Chat, e-mail e notebook/sketchbook

│   └── gateway-or-auth/      # Roteamento / autenticação 

├── banco_dados/                 # Camada 3: Schemas, scripts SQL/NoSQL

└── registro/
    
  ├── logs/                 # Registros de logs e eventos reais da aplicação em execução
  
  └── monitoring/           # Prints
