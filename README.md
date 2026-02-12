# PGATS-02-API

## Testes Funcionais e de Performance em API REST e GraphQL

Projeto focado na implementação de testes automatizados funcionais e não funcionais em uma API bancária simulada.

O sistema permite cadastro de usuários, autenticação via JWT e transferências financeiras entre contas.

O foco principal deste repositório é a validação da qualidade da API.

---

##  Objetivo como QA

Neste projeto foram aplicados:

- Testes funcionais de endpoints REST  
- Testes de autenticação JWT  
- Validação de regras de negócio  
- Testes positivos e negativos  
- Testes de performance com k6  
- Organização modular de suítes de teste  

---

##  Tecnologias Utilizadas

- Node.js  
- Express  
- Swagger  
- Supertest (testes funcionais)  
- k6 (testes de performance)  
- JWT  
- Dotenv  

---

##  Estrutura dos Testes

- `test/` → Testes funcionais REST (Supertest)  
- `performance-tests/` → Testes de performance (k6)  
- `fixtures/` → Massa de dados  
- `helpers/` → Funções reutilizáveis (ex: login)  
- `config/` → Configurações  

---

##  Instalação

### 1. Clone o repositório

```bash
git clone https://github.com/Lucianamachado28/pgats-02-api
cd pgats-02-api
```

### 2. Instale as dependências

```bash
npm install
```
 ###Configuração

Crie um arquivo .env na raiz do projeto:

```bash
BASE_URL=http://localhost:3000
```
### Execução dos Testes Funcionais

Certifique-se de que a API esteja rodando.

```bash
npm test
```

### Execução dos Testes de Performance

```bash
k6 run performance-tests/nome_do_teste.js -e BASE_URL=http://localhost:3000
```
### Para gerar relatório em HTML:

```bash
K6_WEB_DASHBOARD=true K6_WEB_DASHBOARD_EXPORT=html-report.html k6 run performance-tests/nome_do_teste.js -e BASE_URL=http://localhost:3000
```
### Contato
