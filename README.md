# Support System

Frontend do **Support System**, um projeto full-stack para gerenciamento de clientes e chamados de suporte.

O produto foi desenvolvido em dois repositórios:

- Frontend: este repositório
- Backend: https://github.com/yuridomingues/support-system-api

No portfólio, os dois devem ser considerados um único projeto.

## Funcionalidades

- autenticação JWT;
- rotas protegidas;
- cadastro e gerenciamento de clientes;
- CRUD de tickets vinculados a clientes;
- tratamento de erros na interface;
- integração com a API via Axios;
- execução local com Vite ou Docker.

## Stack

- React
- Vite
- React Router
- Axios
- Context API
- Docker

## Rodando localmente

### Vite

```bash
git clone https://github.com/yuridomingues/support-system-interface.git
cd support-system-interface
npm install
npm run dev
```

A aplicação fica disponível em:

```text
http://localhost:5173
```

### Docker

```bash
make run
```

## Arquitetura do produto

```text
React / Vite
     ↓
   Axios
     ↓
FastAPI
     ↓
SQLAlchemy / Alembic
     ↓
PostgreSQL
```

Backend: https://github.com/yuridomingues/support-system-api

## Próxima organização

Frontend e backend pertencem ao mesmo produto. A direção recomendada é consolidá-los futuramente em um monorepo com `frontend/` e `backend/`, preservando o histórico dos dois repositórios atuais.
