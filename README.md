<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0d1117,50:1f6feb,100:58a6ff&height=200&section=header&text=Braian%20de%20Liz%20da%20Silva&fontSize=44&fontColor=ffffff&fontAlignY=38&desc=Desenvolvedor%20de%20sistemas%20com%20foco%20em%20backend&descAlignY=58&descSize=18&animation=twinkling" width="100%" alt="Banner"/>

<img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=22&pause=1000&color=58A6FF&center=true&vCenter=true&width=760&lines=APIs+e+servi%C3%A7os+com+arquitetura+consciente;Performance+medida%2C+n%C3%A3o+presumida;TypeScript+%C2%B7+Node.js+%C2%B7+Bun+%C2%B7+Fastify+%C2%B7+PostgreSQL" alt="Frases em digitação" />

<p>
<img src="https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white" />
<img src="https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=nodedotjs&logoColor=white" />
<img src="https://img.shields.io/badge/Bun-000000?style=for-the-badge&logo=bun&logoColor=white" />
<img src="https://img.shields.io/badge/Fastify-000000?style=for-the-badge&logo=fastify&logoColor=white" />
<img src="https://img.shields.io/badge/PostgreSQL-4169E1?style=for-the-badge&logo=postgresql&logoColor=white" />
<img src="https://img.shields.io/badge/Prisma-2D3748?style=for-the-badge&logo=prisma&logoColor=white" />
<img src="https://img.shields.io/badge/Drizzle-C5F74F?style=for-the-badge&logo=drizzle&logoColor=black" />
<img src="https://img.shields.io/badge/React-61DAFB?style=for-the-badge&logo=react&logoColor=black" />
</p>

<a href="https://portfolio-braian.onrender.com"><img src="https://img.shields.io/badge/Portfolio-58A6FF?style=for-the-badge&logo=googlechrome&logoColor=white" /></a>
<a href="https://www.linkedin.com/in/braian-de-liz-da-silva-47385038b/"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" /></a>

</div>

---

## Como eu tomo decisões técnicas

Escolho stack e arquitetura por medição e pelo custo real de cada camada, não por preferência.

- **Medir antes de escolher.** O TypeMarks nasceu para quantificar quanto a validação de contratos custa em throughput.
- **Arquitetura do tamanho do problema.** No AMOTIF abri mão de camadas MVC que não se pagavam: cada rota é um plugin Fastify que acessa os dados direto, com hooks de autenticação e autorização.
- **Validar na entrada.** Uso schemas executáveis nas rotas, para que dado inválido seja barrado antes de chegar à regra de negócio e ao banco.

---

## Stack

Cada item tem evidência de uso nos projetos abaixo.

| Camada | Tecnologias |
|:--|:--|
| Linguagens | TypeScript, JavaScript |
| Runtime e API | Bun, Node.js, Fastify |
| Dados e validação | PostgreSQL, Prisma, Drizzle, TypeBox, Zod |
| Qualidade | Vitest, Autocannon |

> **Em estudo:** Go (concorrência e profiling), MCP e agentes de IA. Ainda não são domínio consolidado.

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

<br>

<img src="https://streak-stats.demolab.com?user=Braian-de-Liz&theme=github-dark-blue&hide_border=true" alt="Sequência de contribuições" />

<br><br>

<img src="https://github-readme-activity-graph.vercel.app/graph?username=Braian-de-Liz&bg_color=0d1117&color=58a6ff&line=1f6feb&point=ffffff&area=true&hide_border=true" alt="Gráfico de atividade" width="100%" />
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

---

<div align="center">

<sub>Feito com medição antes de decisão.</sub>

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0d1117,50:1f6feb,100:58a6ff&height=120&section=footer" width="100%" alt="" />

</div>
