<p align="center">
  <a href="http://nestjs.com/" target="blank"><img src="https://nestjs.com/img/logo-small.svg" width="120" alt="Nest Logo" /></a>
</p>

# 💰 Fincheck API

O **Fincheck** é uma aplicação de gestão financeira desenvolvida durante o treinamento **JStack**. O objetivo é fornecer uma ferramenta robusta para controle de finanças pessoais e para microempreendedores, utilizando as tecnologias mais modernas do ecossistema Node.js.

## 🚀 Tecnologias

Esse projeto foi desenvolvido com as seguintes tecnologias:

- **[NestJS](https://nestjs.com/)**: Framework Node.js progressivo para construção de aplicações escaláveis.
- **[TypeScript](https://www.typescriptlang.org/)**: Superset do JavaScript que adiciona tipagem estática.
- **[PostgreSQL](https://www.postgresql.org/)**: Banco de dados relacional.
- **[Docker](https://www.docker.com/)**: Para containerização e isolamento do banco de dados.
- **[Prisma ORM](https://www.prisma.io/)**: ORM moderno para modelagem e interação com o banco.

## 💻 Pré-requisitos

Antes de começar, verifique se você atendeu aos seguintes requisitos:
- **Node.js** instalado.
- **Docker Desktop** instalado e rodando (com WSL 2 configurado no Windows).
- Gerenciador de pacotes **Yarn** ou **NPM**.

## 📦 Como rodar o projeto

### 1. Instalar dependências
```bash
yarn install
```

### 2. Configurar o Banco de Dados (Docker)
Para subir o container do PostgreSQL, utilize o comando abaixo:
```bash
docker run --name pg -e POSTGRES_USER=root -e POSTGRES_PASSWORD=root -p 5432:5432 -d postgres
```

### 3. Configurar Variáveis de Ambiente
Certifique-se de ter um arquivo `.env` na raiz do projeto com a string de conexão correta:
```env
DATABASE_URL="postgresql://root:root@localhost:5432/fincheck?schema=public"
```

### 4. Executar Migrations (Prisma)
Para criar as tabelas no banco de dados baseadas no schema:
```bash
npx prisma migrate dev
```

### 5. Iniciar o servidor
```bash
# modo de desenvolvimento
yarn run start:dev

# modo de produção
yarn run start:prod
```

## 🛠️ Ferramentas Úteis

### Prisma Studio
Para visualizar e editar os dados do banco diretamente pelo navegador:
```bash
npx prisma studio
```
##📝 Licença
Esse projeto está sob a licença MIT.

Projeto original por JStack | Implementado para fins de estudo por Theo Guerra, engenheiro de software.
