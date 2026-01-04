Docker: Utilização prática no cenário de Microsserviços
Denilson Bonatti, Instrutor - Digital Innovation One

Muito se tem falado de containers e consequentemente do Docker no ambiente de desenvolvimento. Mas qual a real função de um container no cenários de microsserviços? Qual a real função e quais exemplos práticos podem ser aplicados no dia a dia? Essas são algumas das questões que serão abordadas de forma prática pelo Expert Instructor Denilson Bonatti nesta Live Coding. IMPORTANTE: Agora nossas Live Codings acontecerão no canal oficial da dio._ no YouTube. Então, já corre lá e ative o lembrete! Pré-requisitos: Conhecimentos básicos em Linux, Docker e AWS.

---

# Docker: Utilização prática no cenário de Microsserviços

Projeto desenvolvido com base na Live Coding **“Docker: Utilização prática no cenário de Microsserviços”**, ministrada por **Denilson Bonatti (DIO)**.  
O objetivo deste repositório é aplicar, de forma prática, conceitos fundamentais de **Docker, Docker Compose e microsserviços**, mesmo estando em fase inicial de aprendizado prático.

---

## 🎯 Objetivo do Projeto

Demonstrar na prática:
- O uso de **containers Docker**
- A **orquestração de múltiplos serviços** com Docker Compose
- A comunicação entre serviços
- O uso de **Nginx como proxy reverso / load balancer**
- A execução de uma aplicação simples em ambiente conteinerizado

Este projeto tem **finalidade educacional**, não utilizando dados reais.

---

## 🧩 Arquitetura da Solução

A aplicação é composta por:

- **3 containers de aplicação PHP** (`app1`, `app2`, `app3`)
- **1 container MySQL** para persistência de dados
- **1 container Nginx** atuando como proxy reverso e balanceador de carga
- **1 rede Docker dedicada** para comunicação entre os serviços

O balanceamento de carga é feito pelo Nginx, distribuindo as requisições entre as aplicações.

---

## 📂 Estrutura do Projeto

```bash
.
├── app/
│   └── index.php
├── db/
│   └── banco.sql
├── nginx/
│   ├── Dockerfile
│   └── nginx.conf
├── docker-compose.yml
└── README.md
