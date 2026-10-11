# Sistema de Gestão de Notas

Projeto full-stack para cadastrar alunos, disciplinas e notas, consultar médias e visualizar a situação acadêmica.

## Tecnologias
- API: Node.js, Express, CORS
- Interface: React + Vite
- Persistência: arquivo JSON local (`api/data/db.json`) para facilitar a execução inicial
- Versionamento: Git / GitHub

> Esta versão é pronta para executar localmente. Para uso real em uma escola, recomenda-se migrar a persistência para PostgreSQL, adicionar autenticação/autorização e adequar as regras acadêmicas à instituição.

## Requisitos
- Node.js 18 ou superior
- npm

## Como executar

Abra dois terminais na pasta do projeto.

### 1. API
```bash
cd api
npm install
npm run dev
```
A API inicia em `http://localhost:3001`.

### 2. Interface
Em outro terminal:
```bash
cd ui
npm install
npm run dev
```
Abra o endereço mostrado pelo Vite, normalmente `http://localhost:5173`.

## Funcionalidades
- Cadastrar e remover alunos
- Cadastrar disciplinas
- Registrar, consultar e excluir notas
- Calcular a média por aluno e disciplina
- Exibir situação: Aprovado (média >= 7), Recuperação (média >= 5 e < 7), Reprovado (média < 5)
- Validar campos e notas entre 0 e 10
- Persistir dados localmente em JSON

## Endpoints principais
- `GET /api/health`
- `GET /api/students`, `POST /api/students`, `DELETE /api/students/:id`
- `GET /api/subjects`, `POST /api/subjects`, `DELETE /api/subjects/:id`
- `GET /api/grades`, `POST /api/grades`, `DELETE /api/grades/:id`
- `GET /api/students/:id/summary`

## Repositório remoto
Depois de criar um repositório vazio no GitHub/GitLab:
```bash
git init
git add .
git commit -m "feat: sistema inicial de gestão de notas"
git branch -M main
git remote add origin URL_DO_REPOSITORIO
git push -u origin main
```
