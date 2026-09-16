# Sobre Mim

Olá! Sou **Desenvolvedor Backend em formação**, com formação técnica em **Desenvolvimento de Sistemas** e atualmente cursando **Análise e Desenvolvimento de Sistemas no UniSenai**.

Meu foco está no desenvolvimento de **APIs, sistemas Backend e aplicações orientadas a performance**, principalmente dentro do ecossistema **JavaScript/TypeScript**. Gosto de compreender profundamente as ferramentas que utilizo e entender as decisões técnicas por trás de uma arquitetura, em vez de apenas utilizá-las.

Atualmente trabalho principalmente com **Node.js, Bun e Fastify**, explorando também o **Hono** para serviços menores e de baixo overhead. Paralelamente, venho aprofundando meus estudos em **Go**, linguagem que pretendo dominar especialmente pela sua abordagem para **concorrência, eficiência e construção de serviços Backend**, utilizando também o **Fiber** em meus estudos.

---

## 📊 Atividades no GitHub

<div align="center">

<table>
<tr>
<td align="center">
<strong>Linguagens Mais Usadas</strong><br><br>
<img src="https://github-readme-stats.vercel.app/api/top-langs/?username=Braian-de-Liz&theme=github_dark&layout=compact&hide_border=true" alt="Linguagens mais usadas">
</td>

<td align="center">
<strong>Estatísticas Gerais</strong><br><br>
<img src="https://github-readme-stats.vercel.app/api?username=Braian-de-Liz&theme=github_dark&show_icons=true&hide_border=true&count_private=true" alt="Estatísticas do GitHub">
</td>
</tr>
</table>

</div>

---

## 🛠️ Stack de Desenvolvimento

Minha stack atual é concentrada principalmente em **Backend**, com tecnologias para desenvolvimento de APIs, aplicações web, persistência de dados e validação.

| | | |
|:---:|:---:|:---:|
| <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/typescript/typescript-original.svg" alt="TypeScript" width="40"/><br>**TypeScript** | <img src="https://cdn.simpleicons.org/fastify" alt="Fastify" width="40"/><br>**Fastify** | <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/nodejs/nodejs-original.svg" alt="Node.js" width="40"/><br>**Node.js** |
| Linguagem principal para desenvolvimento Backend type-safe. | Framework Backend focado em baixo overhead e performance. | Runtime consolidado para aplicações JavaScript Backend. |
| <img src="https://bun.sh/logo.svg" alt="Bun" width="40"/><br>**Bun** | <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/postgresql/postgresql-original.svg" alt="PostgreSQL" width="40"/><br>**PostgreSQL** | <img src="https://cdn.simpleicons.org/prisma" alt="Prisma" width="40"/><br>**Prisma** |
| Runtime JavaScript/TypeScript com foco em velocidade e baixo overhead. | Banco de dados relacional utilizado em aplicações Backend. | ORM type-safe para TypeScript e bancos relacionais. |
| <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/javascript/javascript-original.svg" alt="JavaScript" width="40"/><br>**JavaScript** | <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/express/express-original.svg" alt="Express" width="40"/><br>**Express** | <img src="https://cdn.simpleicons.org/drizzle" alt="Drizzle ORM" width="40"/><br>**Drizzle ORM** |
| Linguagem base do ecossistema em que desenvolvo. | Framework para construção de APIs e aplicações web. | ORM SQL-first com forte integração ao TypeScript. |
| <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/mysql/mysql-original.svg" alt="MySQL" width="40"/><br>**MySQL** | <img src="https://cdn.simpleicons.org/zod" alt="Zod" width="40"/><br>**Zod** | <img src="https://raw.githubusercontent.com/sinclairzx81/sinclair-typebox/refs/heads/main/typebox.png" alt="TypeBox" width="40"/><br>**TypeBox** |
| Banco de dados relacional. | Validação e definição de schemas com inferência de tipos. | Definição de schemas JSON com integração ao TypeScript. |

---

## 📚 Próximos Estudos

Tecnologias que fazem parte da minha evolução técnica e que pretendo aprofundar:

| | | |
|:---:|:---:|:---:|
| <img src="https://hono.dev/images/logo.svg" alt="Hono" width="40"/><br>**Hono** | <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/react/react-original.svg" alt="React" width="40"/><br>**React** | <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/nestjs/nestjs-original.svg" alt="NestJS" width="40"/><br>**NestJS** |
| Framework ultraleve para APIs e serviços com baixo overhead. | Biblioteca para construção de interfaces e aplicações web. | Framework Backend para arquiteturas estruturadas e escaláveis. |
| <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/go/go-original.svg" alt="Go" width="40"/><br>**Go** | <img src="./assets/fiber.svg" alt="Fiber" width="40"/><br>**Fiber** | <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/docker/docker-original.svg" alt="Docker" width="40"/><br>**Docker** |
| Linguagem que pretendo dominar com foco em concorrência, eficiência e sistemas Backend. | Framework Go inspirado na ergonomia de frameworks web do ecossistema Express. | Conteinerização e ambientes de execução para aplicações e serviços. |

---

## 💻 Projetos em Destaque

### 🎵 [AMOTIF: Plataforma de Colaboração Musical Assíncrona](https://github.com/Braian-de-Liz)

Plataforma Backend para colaboração musical assíncrona, permitindo que músicos trabalhem em diferentes camadas, versões e projetos sem depender de comunicação em tempo real.

**Stack:** TypeScript, Bun, Fastify, PostgreSQL (NeonDB), Prisma, JWT, Cookies HTTP-only, TypeBox e Render.

**Destaques de Engenharia & Performance:**

- **Performance sob carga com acesso ao banco:** atingiu **+2.900 req/s**, com latência **p99 inferior a 50 ms**, em testes de estresse com alta concorrência e consultas ao banco de dados, sem utilização de cache.
- **Validação de JSON:** atingiu aproximadamente **16.000 req/s** em cenários envolvendo estruturas com arrays aninhados.
- **I/O puro:** atingiu aproximadamente **48.000 req/s** em testes isolados de operações de I/O.
- **Cobertura de testes:** suíte com **+130 testes automatizados**, entre testes unitários e de integração, cobrindo fluxos de sucesso e cenários de exceção.
- **Arquitetura resiliente:** tratamento estruturado de erros, invalidação de sessões por meio de **Cookies HTTP-only**, validação de entrada com **TypeBox** e gerenciamento de arquivos.
- **Backend type-safe:** utilização de **TypeScript + TypeBox + Prisma** para manter consistência entre contratos, validação e acesso aos dados.
- **Banco de dados:** PostgreSQL hospedado na **Neon**, integrado ao Backend por meio do Prisma.
- **Runtime:** desenvolvido sobre **Bun**, utilizando **Fastify** como framework HTTP.

---

### 🚆 [TCHUU-TCHUU: Sistema de Gerenciamento de Ferroramas](https://github.com/Braian-de-Liz/Tchuu-Tchuu)

Ecossistema para gerenciamento e telemetria de uma estrutura ferroviária, utilizando comunicação em tempo real entre diferentes componentes do sistema.

**Stack:** TypeScript, Fastify, PostgreSQL e WebSockets.

**Conceitos aplicados:**

- Sistemas distribuídos
- Comunicação em tempo real
- APIs Backend
- Autenticação
- Arquitetura modular

---

### 📦 [br_standards_with_zod](https://github.com/Braian-de-Liz/br_standards_with_zod)

Biblioteca publicada no npm para validação e normalização de documentos e padrões brasileiros, com integração nativa ao Zod.

[![npm version](https://img.shields.io/npm/v/br_standards_with_zod.svg)](https://www.npmjs.com/package/br_standards_with_zod)
[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](https://opensource.org/licenses/MIT)
[![TypeScript](https://img.shields.io/badge/TypeScript-Ready-blue?logo=typescript)](https://www.typescriptlang.org/)

**Recursos:**

- Validação matemática de CPF e CNPJ
- Validação de CEP e telefone
- Validação de DDD
- Normalização automática de entradas
- Suporte a valores com ou sem máscara
- Integração nativa com Zod
- Build ESM e CommonJS

```ts
import { z } from "zod";
import { zbr } from "br_standards_with_zod";

const userSchema = z.object({
  cpf: zbr.cpf("CPF inválido"),
  tel: zbr.tel("Telefone fora do padrão"),
  cnpj: zbr.cnpj(),
  cep: zbr.cep()
});
