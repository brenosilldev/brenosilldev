# Breno Silva

<p align="center">
  <strong>Desenvolvedor Full Stack — TypeScript, Node.js e React</strong>
</p>

<p align="center">
  Construo aplicações web, APIs REST e sistemas B2B com foco em regras de negócio,
  integrações e processamento assíncrono.
</p>

<p align="center">
  <a href="https://www.linkedin.com/in/brenosilldev/" target="_blank">
    <img src="https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn">
  </a>
  <a href="mailto:brenosill@hotmail.com">
    <img src="https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white" alt="Email">
  </a>
</p>

---

## Atuação

Desenvolvo produtos digitais e sistemas internos utilizando TypeScript, Node.js, React e Next.js.

Minha atuação combina desenvolvimento de APIs, implementação de regras de negócio, integração entre serviços e construção de interfaces administrativas. Também trabalho com processamento assíncrono para operações que exigem desacoplamento, controle de falhas e execução em segundo plano.

No desenvolvimento de sistemas B2B, aplico conceitos como:

- Arquitetura multiempresa;
- Isolamento de dados;
- Autenticação e autorização;
- Integração com serviços externos;
- Processamento assíncrono;
- Idempotência;
- Retry escalonado;
- Dead Letter Queue;
- Reconciliação de processos;
- Separação de responsabilidades.

---

## Tecnologias

**Linguagens:** TypeScript, JavaScript, PHP, Golang  
**Back-end:** Node.js, Express, NestJS, APIs REST  
**Front-end:** React, Next.js, React Query, Tailwind CSS, shadcn/ui  
**Mensageria:** RabbitMQ, exchanges, workers, TTL, retry e Dead Letter Queue  
**Bancos de dados:** MySQL, PostgreSQL, MongoDB, Prisma ORM  
**Infraestrutura e ferramentas:** Docker, Git e GitHub  

---

## Projetos em destaque

### Módulo fiscal de NF-e com RabbitMQ

Desenvolvi a integração de emissão de NF-e ao fluxo de pedidos do PastelTop.

A solução separa a API HTTP do processamento fiscal, permitindo que a comunicação com a SEFAZ seja executada por workers independentes.

**Principais implementações:**

- Processamento assíncrono com RabbitMQ;
- Filas específicas para emissão de NF-e e geração de DANFE;
- Retry escalonado com TTL;
- Dead Letter Exchange e Dead Letter Queue;
- Consumers idempotentes;
- Ack manual e controle de `prefetch`;
- Diferenciação entre falhas técnicas e falhas de negócio;
- Reconciliação automática de processos pendentes;
- Retorno `202 Accepted` para operações em segundo plano.

**Tecnologias:**  
`Node.js` `TypeScript` `Express` `Prisma` `RabbitMQ` `amqplib` `Firebase Storage`

---

### PastelTop — Sistema de gestão para food service

Atuo no desenvolvimento de um sistema B2B para gestão de barracas, produção, pedidos e operações de food service.

**Principais funcionalidades:**

- Ponto de venda;
- Controle de produção;
- Gestão de pedidos e produtos;
- Gestão de usuários, permissões e barracas;
- Geração de documentos PDF;
- Arquitetura multiempresa;
- Isolamento de dados;
- Permissões granulares;
- Auditoria de operações.

**Tecnologias:**  
`Node.js` `TypeScript` `Express` `Prisma` `MySQL` `Next.js` `React` `React Query` `Tailwind CSS` `RabbitMQ`

---

### Sistema de cardápio online

Desenvolvi uma plataforma de cardápio digital para restaurantes, com recursos de apresentação de produtos, localização e gestão de pedidos.

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

Participei do desenvolvimento de uma plataforma de venda de ingressos, trabalhando na integração entre front-end, APIs e serviços de pagamento.

**Principais entregas:**

- Integração com APIs REST desenvolvidas em PHP;
- Implementação de telas a partir de designs;
- Integração de pagamentos;
- Fluxo de confirmação de compra;
- Liberação e disponibilização de ingressos.

**Tecnologias:**  
`PHP` `JavaScript` `jQuery` `APIs REST`

---

## Como trabalho

Transformo requisitos de negócio em soluções técnicas organizadas, considerando:

- Clareza na separação de responsabilidades;
- Manutenibilidade do código;
- Segurança e controle de acesso;
- Consistência dos dados;
- Tratamento de falhas;
- Desacoplamento entre serviços;
- Processamento confiável de operações assíncronas;
- Adequação da arquitetura ao problema real.

---

<p align="center">
  <a href="https://www.linkedin.com/in/brenosilldev/">LinkedIn</a>
  ·
  <a href="mailto:brenosill@hotmail.com">Email</a>
</p>
