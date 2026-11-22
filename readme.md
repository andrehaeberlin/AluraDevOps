# Imersão DevOps - Alura Google Cloud

Este projeto é uma API desenvolvida com FastAPI para gerenciar alunos, cursos e matrículas em uma instituição de ensino.

## Pré-requisitos

- [Python 3.10 ou superior instalado](https://www.python.org/downloads/)
- [Git](https://git-scm.com/downloads)

O Docker não é necessário para a execução local; esta versão não possui Dockerfile.

## Passos para subir o projeto

1. **Faça o download do repositório:**
   [Clique aqui para realizar o download](https://github.com/guilhermeonrails/imersao-devops/archive/refs/heads/main.zip)

2. **Crie um ambiente virtual:**
   ```sh
   python3 -m venv ./venv
   ```

3. **Ative o ambiente virtual:**
   - No Linux/Mac:
     ```sh
     source venv/bin/activate
     ```
   - No Windows PowerShell:
     ```sh
     .\venv\Scripts\Activate.ps1
     ```

   Se a ativação estiver indisponível, use `.\venv\Scripts\python.exe -m pip install -r requirements.txt` e `.\venv\Scripts\python.exe -m uvicorn app:app --reload` sem alterar a política do sistema.

4. **Instale as dependências:**
   ```sh
   pip install -r requirements.txt
   ```

5. **Execute a aplicação:**
   ```sh
   uvicorn app:app --reload
   ```

6. **Acesse a documentação interativa:**

   Abra o navegador e acesse:  
   [http://127.0.0.1:8000/docs](http://127.0.0.1:8000/docs)

   Aqui você pode testar todos os endpoints da API de forma interativa.

---

## Estrutura do Projeto

- `app.py`: Arquivo principal da aplicação FastAPI.
- `models.py`: Modelos do banco de dados (SQLAlchemy).
- `schemas.py`: Schemas de validação (Pydantic).
- `database.py`: Configuração do banco de dados SQLite.
- `routers/`: Diretório com os arquivos de rotas (alunos, cursos, matrículas).
- `requirements.txt`: Lista de dependências do projeto.

## Recursos implementados

| Recurso | Operações |
| --- | --- |
| `/alunos` | Listar, cadastrar, atualizar, remover e consultar por ID, nome ou e-mail |
| `/cursos` | Listar, cadastrar, atualizar e consultar por código |
| `/matriculas` | Cadastrar matrícula e consultar por nome do aluno ou código do curso |

A API usa FastAPI, Pydantic, SQLAlchemy e SQLite. A interface OpenAPI/Swagger está em `/docs`. Esta é uma versão educacional, sem autenticação ou implantação em nuvem configurada neste repositório.

---

- O banco de dados SQLite será criado automaticamente como `escola.db` na primeira execução.
- Para reiniciar o banco, faça backup do arquivo `escola.db` antes de removê-lo: a remoção exclui todos os dados locais.

---
