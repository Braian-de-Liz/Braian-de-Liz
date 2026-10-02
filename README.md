# Braian de Liz da Silva

**Desenvolvedor de sistemas com foco em backend** TypeScript, Bun, Fastify, PostgreSQL

Construo APIs e serviços em JavaScript e TypeScript com atenção a arquitetura, consistência de dados e custo de execução. Decido por medição, não por preferência: comparo alternativas sob carga antes de escolher a stack.

[Portfólio](https://portfolio-braian.onrender.com) · [LinkedIn](https://www.linkedin.com/in/braian-de-liz-da-silva-47385038b/) · contato pelo portfólio

---

## Como eu decido

- **Performance medida, não presumida.** O TypeMarks nasceu para quantificar quanto a validação de contratos custa em throughput.
- **Arquitetura proporcional ao problema.** No AMOTIF abri mão de camadas MVC que não pagavam seu custo: cada rota é um plugin Fastify que acessa os dados diretamente, com hooks para autenticação e autorização.
- **Consistência na fronteira.** Valido na entrada com schemas executáveis, para que dado inválido não chegue à regra de negócio nem ao banco.

---

## Stack

Cada item tem evidência de uso nos projetos abaixo.

| Camada | Tecnologias |
|:--|:--|
| Linguagens | TypeScript, JavaScript |
| Runtime e API | Bun, Node.js, Fastify |
| Dados e validação | PostgreSQL, Prisma, TypeBox, Zod |
| Qualidade | Vitest, Autocannon |

**Em estudo:** Go (concorrência e profiling), MCP e agentes de IA. Ainda não são domínio consolidado.

---

## GitHub

<div align="center">
<table>
<tr>
<td align="center">
<strong>Linguagens mais usadas</strong><br><br>
<img src="https://github-readme-stats.vercel.app/api/top-langs/?username=Braian-de-Liz&theme=github_dark&layout=compact&hide_border=true" alt="Linguagens mais usadas">
</td>
<td align="center">
<strong>Estatísticas gerais</strong><br><br>
<img src="https://github-readme-stats.vercel.app/api?username=Braian-de-Liz&theme=github_dark&show_icons=true&hide_border=true&count_private=true" alt="Estatísticas do GitHub">
</td>
</tr>
</table>
</div>

---

## Projetos

### [AMOTIF](https://github.com/Braian-de-Liz/AMOTIF) · [aplicação](https://amotif-music.onrender.com)

Plataforma de colaboração musical assíncrona. Cada contribuição entra como uma camada de áudio versionada, preservando autoria e histórico em vez de sobrescrever o trabalho anterior.

**Stack:** Bun · Fastify 5 · TypeBox (JIT) · Prisma 7 · PostgreSQL · JWT + Argon2id · Supabase Storage · React 19

- 40+ endpoints, 14 modelos Prisma, 15 migrações
- Upload de áudio de até 40 MB transmitido por streaming ao storage, sem passar pela memória da API; só a URL final é persistida
- Em teste de carga com acesso real ao banco e sem cache: `+2.900 req/s` com `p99 < 50 ms`
- `+130 testes` automatizados (unitários e integração)

---

### [TypeMarks](https://github.com/Braian-de-Liz/typemarks)

Benchmark de 15 cenários combinando runtimes, frameworks e validadores, para medir quanto a validação de contratos custa em throughput e tornar a escolha de stack uma decisão com dado.

**Stack:** Bun · Node.js · Hono · Fastify · AJV · Autocannon

| Runtime | Framework | Validador | req/s | Latência média |
|:--|:--|:--|--:|--:|
| Bun | Hono | AJV | 28.534 | 2,94 ms |
| Bun | Elysia | TypeBox | 25.915 | 3,45 ms |
| Bun | Hono | Schema-Shield | 25.021 | 3,61 ms |
| Bun | Fastify | AJV | 22.527 | 3,93 ms |
| Node | Fastify | AJV | 14.998 | 6,16 ms |

Melhor cenário com P99 de 5,60 ms. A diferença entre as duas últimas linhas isola o efeito do runtime: **+50,2% do Bun sobre o Node.js** com a mesma combinação Fastify + AJV.

---

### [br_standards_with_zod](https://github.com/Braian-de-Liz/br_standards_with_zod) · [npm](https://www.npmjs.com/package/br_standards_with_zod) · [demo](https://zbr-view-7bc2.vercel.app/)

Validação de documentos brasileiros além de regex: o dígito verificador é calculado por módulo 11 e a entrada é normalizada antes de chegar ao schema, com integração nativa ao Zod.

[![npm version](https://img.shields.io/npm/v/br_standards_with_zod.svg)](https://www.npmjs.com/package/br_standards_with_zod)
[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](https://opensource.org/licenses/MIT)
[![TypeScript](https://img.shields.io/badge/TypeScript-Ready-blue?logo=typescript)](https://www.typescriptlang.org/)

```ts
import { z } from "zod";
import { zbr } from "br_standards_with_zod";

const cadastro = z.object({
  cpf: zbr.cpf(),
  cnpj: zbr.cnpj(),
  tel: zbr.tel(),
});

// "123.456.789-09" -> normalizado para "12345678909"
// "111.111.111-11" -> rejeitado: sequência inválida
```

Zero dependências em runtime · build ESM e CommonJS · testes com Vitest

---

### [Tchuu-Tchuu](https://github.com/Braian-de-Liz/Tchuu-Tchuu)

Monitoramento ferroviário em que a telemetria de sensores chega por WebSocket e alimenta um painel operacional. Três componentes com escala e deploy independentes.

**Stack:** Node.js · Fastify · WebSocket · JWT · PostgreSQL (Neon) · Chart.js

- 881 commits
- Frontend em JavaScript puro, escolha deliberada para exercitar fundamentos
- CORS restrito ao domínio do próprio frontend
