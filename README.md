# Breno Silva

<p align="center">
  <strong>Desenvolvedor Full Stack | TypeScript, Node.js e React</strong>
</p>

<p align="center">
  APIs B2B · Integrações · SaaS · Processamento assíncrono
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

## Atuação

Desenvolvo aplicações web, APIs REST e sistemas B2B utilizando TypeScript, Node.js, React e Next.js.

Minha atuação envolve implementação de regras de negócio, autenticação, autorização, integrações com serviços externos, arquitetura multiempresa e processamento assíncrono com foco em confiabilidade e manutenção.

Também trabalho na construção de interfaces administrativas e na integração entre front-end, back-end, bancos de dados e serviços de mensageria.

---

## Tecnologias

**Back-end:** Node.js, TypeScript, Express, NestJS e APIs REST  
**Front-end:** React, Next.js, React Query, Tailwind CSS e shadcn/ui  
**Mensageria:** RabbitMQ, workers, retry, TTL e Dead Letter Queue  
**Bancos de dados:** MySQL, PostgreSQL, MongoDB e Prisma ORM  
**Infraestrutura:** Docker, Git e GitHub  
**Linguagens utilizadas:** TypeScript, JavaScript e PHP  
**Em aprofundamento:** Golang, arquitetura orientada a eventos e sistemas distribuídos

---

## Projetos em destaque

### Módulo fiscal de NF-e com RabbitMQ

Atuação no desenvolvimento de uma integração de emissão de NF-e conectada ao fluxo de pedidos do PastelTop.

A solução separa a API HTTP do processamento fiscal, permitindo a execução da comunicação com a SEFAZ por workers independentes.

**Principais implementações:**

- APIs para solicitação e acompanhamento da emissão;
- Processamento assíncrono com RabbitMQ;
- Filas específicas para emissão de NF-e e geração de DANFE;
- Retry escalonado com TTL;
- Dead Letter Exchange e Dead Letter Queue;
- Consumers idempotentes;
- Ack manual e controle de `prefetch`;
- Tratamento separado para falhas técnicas e de negócio;
- Reconciliação automática de processos pendentes;
- Retorno `202 Accepted` para operações em segundo plano.

**Tecnologias:**  
`Node.js` `TypeScript` `Express` `Prisma` `RabbitMQ` `amqplib` `Firebase Storage`

---

### PastelTop — Sistema de gestão para food service

Atuação no desenvolvimento de um sistema B2B para gestão de barracas, produção, pedidos e operações de food service.

**Principais funcionalidades:**

- Ponto de venda;
- Controle de produção;
- Gestão de pedidos e produtos;
- Gestão de usuários, permissões e barracas;
- Arquitetura multiempresa;
- Isolamento de dados;
- Permissões granulares;
- Auditoria de operações;
- Geração de documentos PDF;
- Processamento assíncrono de operações críticas.

**Tecnologias:**  
`Node.js` `TypeScript` `Express` `Prisma` `MySQL` `Next.js` `React` `React Query` `Tailwind CSS` `RabbitMQ`

---

### Sistema de cardápio online

Desenvolvimento de uma plataforma de cardápio digital para restaurantes, com gestão de produtos, pedidos e estabelecimentos.

**Principais funcionalidades:**

- Cardápio online;
- Painel administrativo;
- Gestão de pedidos;
- Autenticação com JWT;
- Cálculo de frete;
- Localização de estabelecimentos;
- Interface responsiva;
- Integração com Google Maps.

**Tecnologias:**  
`Node.js` `Express` `Prisma` `MySQL` `React` `Next.js` `React Query` `JWT`

---

### Sistema de venda de ingressos

Participação no desenvolvimento de uma plataforma de venda de ingressos, atuando na integração entre interfaces, APIs e serviços de pagamento.

**Principais entregas:**

- Integração com APIs REST desenvolvidas em PHP;
- Implementação de interfaces a partir de designs;
- Integração com serviços de pagamento;
- Fluxo de confirmação de compras;
- Liberação de ingressos após confirmação do pagamento.

**Tecnologias:**  
`PHP` `JavaScript` `jQuery` `APIs REST`

---

## Princípios técnicos

- Separação de responsabilidades;
- Código organizado e manutenível;
- APIs claras e consistentes;
- Tratamento explícito de falhas;
- Processamento assíncrono confiável;
- Idempotência em operações críticas;
- Consistência e isolamento de dados;
- Controle de acesso baseado em permissões;
- Arquitetura adequada ao problema de negócio.

---

## Contato

<p align="center">
  <a href="https://www.linkedin.com/in/brenosilldev/" target="_blank">LinkedIn</a>
  ·
  <a href="mailto:brenosill@hotmail.com">Email</a>
</p>
