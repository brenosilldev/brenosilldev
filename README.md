# Breno Silva

<p align="center">
  <strong>Desenvolvedor Back-end | Node.js, TypeScript e NestJS</strong>
</p>

<p align="center">
  Desenvolvendo APIs REST, sistemas SaaS B2B, integrações e aplicações web orientadas a produto.
</p>

<p align="center">
  <a href="https://www.linkedin.com/in/brenosilldev/" target="_blank">
    <img src="https://img.shields.io/badge/LinkedIn-Perfil-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn">
  </a>
  <a href="mailto:brenosill@hotmail.com">
    <img src="https://img.shields.io/badge/Email-Contato-D14836?style=for-the-badge&logo=gmail&logoColor=white" alt="Email">
  </a>
</p>

---

## Sobre mim

Sou Desenvolvedor Full Stack com cerca de 3 anos de experiência prática no desenvolvimento de aplicações web, sistemas B2B e soluções orientadas a produto.

Minha principal atuação está no back-end com Node.js, TypeScript, Express e NestJS, desenvolvendo APIs REST, regras de negócio, autenticação, controle de acesso, integrações com serviços externos e processos assíncronos.

Também trabalho com React e Next.js na construção de dashboards, painéis administrativos e interfaces para aplicações web.

Tenho experiência prática com:

- APIs REST;
- sistemas SaaS;
- arquitetura multi-empresa e multi-tenant;
- autenticação com JWT;
- controle de acesso baseado em papéis;
- integração com APIs externas;
- processamento assíncrono com RabbitMQ;
- workers independentes;
- retry com TTL;
- Dead Letter Queue;
- idempotência;
- reconciliação de processos;
- modelagem e acesso a bancos de dados.

Gosto de entender o problema de negócio antes de escolher a solução técnica, avaliando decisões como separação entre API e worker, uso de filas, estratégias de retry e organização das responsabilidades da aplicação.

---

## Tecnologias e ferramentas

### Linguagens

![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black)
![Go](https://img.shields.io/badge/Go-00ADD8?style=flat-square&logo=go&logoColor=white)

### Back-end

![Node.js](https://img.shields.io/badge/Node.js-339933?style=flat-square&logo=node.js&logoColor=white)
![Express](https://img.shields.io/badge/Express-000000?style=flat-square&logo=express&logoColor=white)
![NestJS](https://img.shields.io/badge/NestJS-E0234E?style=flat-square&logo=nestjs&logoColor=white)

- APIs REST
- Autenticação com JWT
- Controle de acesso por papéis
- Service Layer
- Arquitetura MVC
- TypeScript aplicado ao back-end

### Mensageria e processamento assíncrono

![RabbitMQ](https://img.shields.io/badge/RabbitMQ-FF6600?style=flat-square&logo=rabbitmq&logoColor=white)

- Exchanges e filas
- Workers independentes
- Ack manual
- Prefetch
- Retry com TTL
- Dead Letter Queue
- Retry escalonado
- Idempotência
- Reconciliação de processos
- Arquitetura orientada a eventos

### Bancos de dados e ORM

![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=flat-square&logo=mysql&logoColor=white)
![MongoDB](https://img.shields.io/badge/MongoDB-47A248?style=flat-square&logo=mongodb&logoColor=white)
![Prisma](https://img.shields.io/badge/Prisma-2D3748?style=flat-square&logo=prisma&logoColor=white)

### Front-end

![React](https://img.shields.io/badge/React-20232A?style=flat-square&logo=react&logoColor=61DAFB)
![Next.js](https://img.shields.io/badge/Next.js-000000?style=flat-square&logo=next.js&logoColor=white)
![React Query](https://img.shields.io/badge/React_Query-FF4154?style=flat-square&logo=reactquery&logoColor=white)
![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-06B6D4?style=flat-square&logo=tailwindcss&logoColor=white)
![shadcn/ui](https://img.shields.io/badge/shadcn%2Fui-000000?style=flat-square&logo=shadcnui&logoColor=white)

### Ferramentas

![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![Git](https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white)
![GitHub](https://img.shields.io/badge/GitHub-181717?style=flat-square&logo=github&logoColor=white)

---

## Projetos relevantes

### Módulo Fiscal de NF-e com RabbitMQ

Integração desenvolvida para o PastelTop com o objetivo de automatizar a emissão de Nota Fiscal Eletrônica diretamente a partir do fluxo de pedidos.

A solução desacopla a comunicação com a SEFAZ da resposta HTTP entregue ao usuário, permitindo que o processamento fiscal aconteça de forma assíncrona.

#### Principais decisões técnicas

- Separação entre a API HTTP e o worker consumidor de filas;
- Comunicação entre API e worker exclusivamente por RabbitMQ;
- Exchange principal para distribuição das mensagens;
- Filas separadas para emissão de NF-e e geração de DANFE;
- Filas de retry escalonado com TTL de 30 segundos, 2 minutos e 10 minutos;
- Dead Letter Exchange e Dead Letter Queue;
- Consumers idempotentes;
- `prefetch(1)` e ack manual;
- Separação entre falhas técnicas e falhas de negócio;
- Job de reconciliação executado a cada 5 minutos;
- Retorno `202 Accepted` para processamento em segundo plano.

#### Tecnologias utilizadas

- Node.js
- TypeScript
- Express
- Prisma
- RabbitMQ
- `amqplib`
- Firebase Storage
- Integração com SEFAZ por meio da `nfewizard-io`

#### Resultado técnico

A emissão fiscal passou a ser processada em background, sem bloquear o fluxo de pedidos. A arquitetura também permite tratar falhas temporárias da SEFAZ, indisponibilidade do worker e mensagens que precisam ser encaminhadas para análise.

> A publicação de detalhes deste projeto deve respeitar as regras de confidencialidade da empresa e dos serviços integrados.

---

### PastelTop — Sistema de gestão para food service

Sistema de gestão para barracas e produção de pastéis, com funcionalidades voltadas ao controle operacional, gestão de pedidos, produção e administração de unidades.

#### Funcionalidades

- PDV — Ponto de Venda;
- Controle de produção;
- Gestão de pedidos e produtos;
- Gestão de usuários e permissões;
- Gestão de barracas;
- Geração de documentos PDF;
- Arquitetura multi-empresa;
- Isolamento de dados entre empresas;
- Permissões granulares;
- Auditoria de operações.

#### Destaques técnicos

- Back-end estruturado com Node.js, TypeScript e Express;
- Arquitetura MVC com Service Layer;
- Type Safety com TypeScript;
- Persistência utilizando Prisma e MySQL;
- Front-end com Next.js, React, Tailwind CSS e shadcn/ui;
- Gerenciamento de dados com React Query;
- Processamento assíncrono com RabbitMQ;
- Paginação;
- Cache;
- Autenticação e controle de acesso.

#### Tecnologias utilizadas

`Node.js` `TypeScript` `Express` `Prisma` `MySQL` `Next.js` `React` `Tailwind CSS` `shadcn/ui` `React Query` `RabbitMQ`

---

### Sistema de cardápio online

Sistema de cardápio digital para restaurantes, com recursos para apresentação de produtos, gestão de pedidos e administração de estabelecimentos.

#### Funcionalidades

- Cardápio online;
- Localização de estabelecimentos;
- Cálculo automático de frete;
- Autenticação com JWT;
- Painel administrativo;
- Gerenciamento de pedidos;
- Interface responsiva.

#### Tecnologias utilizadas

`Node.js` `Express` `Prisma` `MySQL` `JWT` `React` `Next.js` `React Query` `Google Maps API`

---

### Sistema de venda de ingressos

Atuação no desenvolvimento de um sistema de venda de ingressos, com foco em integração de APIs, pagamentos e experiência do usuário.

#### Responsabilidades

- Integração com APIs REST desenvolvidas em PHP;
- Implementação de telas a partir de designs fornecidos;
- Integração com meios de pagamento;
- Desenvolvimento do fluxo de liberação de ingressos;
- Disponibilização dos pedidos após a confirmação da compra.

#### Tecnologias utilizadas

`PHP` `JavaScript` `jQuery` `APIs REST`

---

## Princípios técnicos

Durante o desenvolvimento dos projetos, procuro aplicar:

- Separação de responsabilidades;
- Código organizado e de fácil manutenção;
- Tipagem estática com TypeScript;
- Validação de dados;
- Autenticação e autorização;
- Tratamento explícito de erros;
- Idempotência em processos assíncronos;
- Uso de filas para desacoplamento;
- Retry apenas para falhas recuperáveis;
- Separação entre falhas técnicas e falhas de negócio;
- Modelagem de dados orientada às regras do produto.

---

## Atualmente estudando

- Arquitetura orientada a eventos;
- Mensageria e processamento assíncrono;
- Sistemas distribuídos;
- Boas práticas para APIs;
- Golang aplicado ao desenvolvimento back-end;
- Resiliência e confiabilidade de aplicações.

---

## Objetivo profissional

Tenho interesse em oportunidades como:

- Desenvolvedor Back-end;
- Desenvolvedor Node.js;
- Desenvolvedor TypeScript;
- Desenvolvedor NestJS;
- Desenvolvedor Full Stack.

Busco atuar no desenvolvimento de produtos SaaS, plataformas B2B, integrações, sistemas distribuídos e aplicações web orientadas a problemas reais de negócio.

---

## Vamos conversar?

Se você trabalha com engenharia de software, produtos digitais ou recrutamento tech, fique à vontade para se conectar comigo pelo [LinkedIn](https://www.linkedin.com/in/brenosilldev/).

<p align="center">
  <a href="https://www.linkedin.com/in/brenosilldev/">LinkedIn</a>
  ·
  <a href="mailto:brenosill@hotmail.com">Email</a>
</p>
