PGATS-02-API


Testes Funcionais e de Performance em API REST e GraphQL


   Sobre o Projeto     

Projeto focado na implementação de testes automatizados funcionais e não funcionais em uma API bancária simulada, utilizando boas práticas de organização e estrutura de testes.

O sistema permite cadastro de usuários, autenticação via JWT e transferências financeiras entre contas.

O foco principal deste repositório é a validação da qualidade da API.


  Objetivo como QA
  
Neste projeto foram aplicados:

Testes funcionais de endpoints REST

Testes de autenticação JWT

Validação de regras de negócio

Testes positivos e negativos

Testes de performance com k6

Organização modular de suites de teste


  Tecnologias Utilizadas

Node.js

Express

Swagger

Supertest (testes funcionais)

k6 (testes de performance)

JWT

Dotenv


  Estrutura dos Testes
  
test/                → Testes funcionais REST (Supertest)
performance-tests/   → Testes de performance (k6)
fixtures/            → Massa de dados
helpers/             → Funções reutilizáveis (ex: login)
config/              → Configurações


  Principais Cenários Validados
  
Registro de Usuário

  Impede usuários duplicados

  Valida campos obrigatórios

Login

  Valida autenticação correta
  
  Bloqueia credenciais inválidas

  Geração de token JWT

Transferências

  Validação de saldo

  Restrição para valores acima de R$ 5.000

  Testes de fluxo completo

  Testes negativos


  Testes de Performance

Testes realizados com k6 para avaliar:

Tempo médio de resposta

Taxa de falhas

Comportamento sob carga simultânea

Execução:

k6 run performance-tests/nome_do_teste.js -e BASE_URL=http://localhost:3000

  Execução

1️⃣ Instalar dependências

npm install


2️⃣ Criar .env

BASE_URL=http://localhost:3000


3️⃣ Rodar testes funcionais

npm test



Luciana de Souza Machado
Pós-graduanda em Engenharia de Software
Mentoria em Testes de Software – Júlio de Lima
Transição para Qualidade de Software (QA)
