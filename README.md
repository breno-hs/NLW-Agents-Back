# NLW Agents

Projeto desenvolvido durante o evento da **Rocketseat** para demonstrar o uso de agentes inteligentes criando uma API robusta e eficiente.

## 🚀 Tecnologias

- **Node.js** com TypeScript (experimental strip types)
- **Fastify** - Framework web rápido e eficiente
- **Drizzle ORM** - Type-safe database toolkit
- **PostgreSQL** com extensão **pgvector**
- **Zod** - Validação de esquemas TypeScript
- **Biome** - Linter e formatador de código
- **Docker** - Containerização do banco de dados

## 🏗️ Arquitetura

O projeto segue uma arquitetura modular com:

- **Separação de responsabilidades** entre rotas, schemas e conexão com banco
- **Validação de schemas** com Zod para type safety
- **ORM type-safe** com Drizzle para operações de banco de dados
- **Validação de variáveis de ambiente** centralizadas

## ⚙️ Setup e Configuração

### Pré-requisitos

- Node.js 20+ (versão com suporte a `--experimental-strip-types`)
- Docker e Docker Compose

### 1. Clone o repositório

```bash
git clone <url-do-repositorio>
cd "server"
```

### 2. Configure o Banco de Dados

```bash
docker-compose up -d
```

### 3. Configure as variáveis de ambite

Crie um arquivo `.env` na raiz do projeto:

```bash
PORT=3333
DATABASE_URL=postgresql://docker:docker@localhost:5432/agents
```

### 4. Instale as dependências

```bash
npm install
```

### 5. Execute as migrações do banco

```bash
npx drizzle-kit migrate
```

### 6. (Opcional) Popule o banco com dados de exemplo

```bash
npm run db:seed
```

### 7. Execute o projeto

Desenvolvimento:

```bash
npm run dev
```

Produção:

```bash
npm start
```

## 📝 Scripts Disponíveis

- `npm run dev` - Executa o servidor em modo de desenvolvimento com hot reload
- `npm start` - Executa o servidor em modo produção
- `npm run db:seed` - Popula o banco de dados com dados de exemplo

### Endpoints

A API estará disponível em `http://localhost:3333`

- `GET /health` - Health check da aplicação
- `GET /rooms` - Lista as salas disponíveis

---

Desenvolvido durante a NLW da Rocketseat
