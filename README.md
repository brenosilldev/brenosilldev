# 👨‍💻 Breno Silva

<p align="center">
  <b>Desenvolvedor Full Stack — TypeScript/JavaScript, Golang & Sistemas Distribuídos</b>
</p>

<p align="center">
  <a href="https://www.linkedin.com/in/brenosilldev/" target="_blank"><img src="https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white"/></a>
  <a href="mailto:brenosill@hotmail.com"><img src="https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white"/></a>
</p>

---

## 👋 Sobre mim

Sou **Desenvolvedor Full Stack** com cerca de **3 anos de experiência prática**, construindo aplicações web escaláveis e sistemas B2B orientados a produto. Trabalho no dia a dia com **React, Next.js, Node.js e NestJS**, do front-end performático a **APIs robustas e prontas para produção**.

Nos últimos meses venho aprofundando **arquitetura orientada a eventos, mensageria (RabbitMQ) e Golang**, aplicando esses conceitos em processos assíncronos reais — como emissão fiscal integrada a sistemas externos — e não apenas em CRUDs tradicionais.

Gosto de resolver problemas de negócio com **arquitetura limpa, separação de responsabilidades e decisões técnicas justificadas** (por que uma fila, por que um retry com backoff, por que separar um worker da API) — não só entregar funcionalidade, mas entender o *porquê* por trás dela.

---

## 🛠️ Tecnologias & Ferramentas

**Linguagens:** TypeScript, JavaScript, Golang <br>
**Back-end:** Node.js, Express, NestJS, APIs REST, arquitetura orientada a eventos <br>
**Mensageria:** RabbitMQ (exchanges, filas, retry com TTL, Dead Letter Queue) <br>
**Banco de dados:** PostgreSQL, MySQL, MongoDB, Prisma ORM <br>
**Front-end:** React, Next.js, React Query, Tailwind CSS, shadcn/ui <br>
**Outros:** Docker, Git, GitHub, JWT

---

## 🚀 Projetos Relevantes

### 📄 Módulo Fiscal (NF-e) com RabbitMQ — PastelTop

Projeto que integrei ao PastelTop para automatizar a **emissão de Nota Fiscal Eletrônica (NF-e)** direto do fluxo de pedidos, desacoplando a chamada à SEFAZ (lenta e sujeita a falhas) da resposta ao usuário através de **processamento assíncrono orientado a eventos**.

**Stack:**

* Back-end: Node.js, TypeScript, Express, Prisma
* Mensageria: RabbitMQ (`amqplib`)
* Integrações: SEFAZ (via `nfewizard-io`, certificado digital A1), Firebase Storage

**Arquitetura:**

* Separação entre `api` (HTTP) e `worker` (consumidor de filas), como processos independentes — a API nunca fala diretamente com o worker, só via RabbitMQ
* Topologia dedicada: exchange principal, filas de emissão e de geração de DANFE, exchange de dead-letter e filas de retry escalonado (30s → 2min → 10min) usando TTL, sem nenhum `setTimeout` na aplicação
* Consumers idempotentes com `prefetch(1)` e ack manual, para lidar com a entrega "pelo menos uma vez" do RabbitMQ sem duplicar processamento
* Separação entre falha técnica (vai para retry) e falha de negócio (vai direto para a DLQ, sem desperdiçar tentativas)
* Job de reconciliação (cron a cada 5 min) como rede de segurança para notas presas em estados intermediários

**Resultado:** a emissão de NF-e responde `202 Accepted` imediatamente ao usuário, com o processamento pesado acontecendo em background — sem travar o fluxo de pedidos e com resiliência a falhas da SEFAZ e a quedas do próprio worker.

---

### 🍽️ Sistema de Cardápio Online

Sistema de **cardápio digital** para restaurantes, focado em performance, usabilidade e gestão de pedidos.

**Stack:**

* Back-end: Node.js, Express, Prisma, MySQL, JWT
* Front-end: React, Next.js, React Query
* Integrações: Google Maps API

**Principais funcionalidades:**

* Cardápio online com localização de estabelecimentos
* Cálculo automático de frete
* Autenticação segura com JWT
* Painel administrativo para gerenciamento de pedidos
* Plataforma responsiva e de fácil manutenção

---

### 🚀 PastelTop – Sistema de Gestão para Food Service

Sistema completo para **gestão de barracas e produção de pastéis**, com foco em controle operacional, segurança e escalabilidade — inclui o módulo fiscal assíncrono descrito acima.

**Stack:**

* Back-end: Node.js, TypeScript, Express, Prisma, MySQL
* Front-end: Next.js 15, React 18, TypeScript, Tailwind CSS, shadcn/ui
* Estado e dados: React Query

**Funcionalidades principais:**

* PDV (Ponto de Venda) completo
* Controle de produção com geração de PDFs
* Gestão de pedidos, produtos, usuários e barracas
* Arquitetura multi-empresa com isolamento de dados
* Sistema de permissões granulares e auditoria completa

**Destaques técnicos:**

* Arquitetura MVC com Service Layer
* Type Safety completo com TypeScript
* Processamento assíncrono via RabbitMQ para operações críticas (emissão fiscal)
* Paginação, cache e boas práticas de segurança

---

### 🎟️ Sistema de Venda de Ingressos

Atuação no desenvolvimento de um **sistema de venda de ingressos**, com foco em integração de APIs, pagamentos e experiência do usuário.

**Responsabilidades:**

* Integração completa com APIs REST desenvolvidas em PHP puro
* Implementação das telas conforme design fornecido
* Integração de pagamentos
* Fluxo de liberação e disponibilização de ingressos após a compra

**Tecnologias:** PHP, JavaScript, jQuery, APIs REST
