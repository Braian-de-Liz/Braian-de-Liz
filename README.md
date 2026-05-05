# Sobre Mim

Olá! Sou estudante do **1º ano do Curso de Analise e Desenvolvimento de Sistemas no UniSenai**, apaixonado por tecnologia e em constante evolução no mundo da programação. Atualmente focado no desenvolvimento de aplicações de alta performance e sistemas escaláveis.

---

## 📊 Atividades no Github

<center>
    <td align="center">
      <strong>Linguagens Mais Usadas</strong><br>
      <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=Braian-de-Liz&theme=github_dark&layout=compact&hide_border=true" alt="Top Langs">
    </table>
    <td align="center">
      <strong>Estatísticas Gerais</strong><br>
      <img src="https://github-readme-stats.vercel.app/api?username=Braian-de-Liz&theme=github_dark&show_icons=true&hide_border=true&count_private=true" alt="GitHub Stats">
    </td>
   </tr>
</table>
</center>

---

## 🛠️ Stack de Desenvolvimento

Minha "caixa de ferramentas" atual para o desenvolvimento Full-Stack:

- <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/typescript/typescript-original.svg" alt="Typescript" width="20"/> **TypeScript** — Base para construção de aplicações robustas e tipadas.
- <img src="https://fastify.dev/img/logos/fastify-white.svg" alt="Fastify" width="20"/> **Fastify** — Framework back-end focado em performance e baixo overhead.
- <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/nodejs/nodejs-original.svg" alt="Node.js" width="20"/> **Node.js** — Runtime principal de desenvolvimento.
- <img src="https://bun.sh/logo.svg" alt="Bun" width="20"/> **Bun** — runtimes de execução Javascript, focado em performance e recursos inclusos.
- <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/postgresql/postgresql-original.svg" alt="PostgreSQL" width="20"/> **PostgreSQL** — Banco de dados relacional (SQL) para persistência de dados.
- <img src="https://cdn.simpleicons.org/drizzle" alt="Drizzle ORM" width="20"/> **Drizzle ORM** — TypeScript ORM que combina a performance do SQL nativo com segurança de tipos em tempo de compilação, eliminando o overhead de abstrações pesadas.
- <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/express/express-original.svg" alt="Express" width="20"/> **Express** — Framework para APIs e middleware.
- <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/mysql/mysql-original.svg" alt="MySQL" width="20"/> **MySQL** — Gerenciamento de bancos de dados relacionais.
- <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/javascript/javascript-original.svg" alt="JavaScript" width="20"/> **JavaScript (ES6+)**
- <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/html5/html5-original.svg" alt="HTML5" width="20"/> **HTML5**  
- <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/css3/css3-original.svg" alt="CSS3" width="20"/> **CSS3**
- <img src="https://zod.dev/logo.svg" alt="Zod" width="20"/> **Zod** — Validação de dados com segurança e inferência de tipos em TypeScript.
- <img src="https://github.com/sinclairzx81/typebox/raw/master/typebox.png" alt="TypeBox" width="20"/> **TypeBox** — Geração de schemas e validação performática para aplicações JSON.

---

## 📚 Próximos Estudos

Expandindo meu conhecimento técnico para novas ferramentas:

- <img src="https://raw.githubusercontent.com/elysiajs/elysia/main/assets/elysia_lucia.png" alt="Elysia" width="20"/> **ElysiaJS** — Framework focado em performance extrema e integração nativa com Bun.
- <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/react/react-original.svg" alt="React" width="20"/> **React** — Bibliotecas de interface modernas para SPAs.
- <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/nestjs/nestjs-original.svg" alt="NestJS" width="20"/> **Nest.js** — Framework opinativo para arquiteturas de back-end escaláveis.
- <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/python/python-original.svg" alt="Python" width="20"/> **Python**
- <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/csharp/csharp-original.svg" alt="C#" width="20"/> **C#**
- <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/go/go-original.svg" alt="Go" width="20"/> **Go** — Linguagem de alta performance para sistemas concorrentes e escaláveis.

---

### 💼 Projetos em Destaque

- 🚆 **[TCHUU-TCHUU - Sistema de Gerenciamento de Ferroramas](https://github.com/Braian-de-Liz/Tchuu-Tchuu)** — Ecossistema completo de telemetria e gestão ferroviária.  

  ✅ **Stack:** TypeScript, Fastify, PostgreSQL e WebSockets.  
  ✅ **Arquitetura:** Microserviços (Frontend, Backend e DB independentes).  
  ✅ **Segurança:** Autenticação JWT e hashing de senhas.  

  → Meu projeto principal que aplica **Sistemas Distribuídos** e **Engenharia de Software**.

- 📦 **[br_standards_with_zod](https://github.com/Braian-de-Liz/br_standards_with_zod)** — Biblioteca npm para validação de documentos brasileiros com integração nativa ao Zod.

  [![npm version](https://img.shields.io/npm/v/br_standards_with_zod.svg)](https://www.npmjs.com/package/br_standards_with_zod)
  [![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](https://opensource.org/licenses/MIT)
  [![TypeScript](https://img.shields.io/badge/TypeScript-Ready-blue?logo=typescript)](https://www.typescriptlang.org/)

  ✅ **Validação real:** Cálculo matemático de dígitos verificadores (CPF, CNPJ).  
  ✅ **Padrões oficiais:** DDDs da Anatel e nono dígito para celulares.  
  ✅ **Aceita máscara ou não:** Normalização automática de entradas.  
  ✅ **Transformação automática:** Retorno apenas números/letras relevantes.  
  ✅ **Integração nativa com Zod:** Sem necessidade de `refine` manual.  
  ✅ **Dual build:** Compatível com ESM e CommonJS.  

  ```typescript
  import { z } from 'zod';
  import { zbr } from 'br_standards_with_zod';

  const userSchema = z.object({
    cpf: zbr.cpf("CPF inválido"),
    tel: zbr.tel("Telefone fora do padrão"),
    cnpj: zbr.cnpj(),
    cep: zbr.cep()
  });
´´´
Minha primeira biblioteca pública no npm, demonstrando TypeScript avançado, integração com ecossistema Zod e publicação de pacotes.



 Vamos nos conectar?
 E-mail: delizbraian@gmail.com

 LinkedIn: Braian De Liz da Silva

 WhatsApp: +55 (47) 93380-3828
