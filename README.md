FastAPI Users API
API REST para gerenciamento de usuários, desenvolvida com FastAPI, utilizando SQLite como banco de dados, SQLAlchemy como ORM e autenticação baseada em JWT.
Este projeto foi criado com foco em organização, separação de responsabilidades e aplicação de boas práticas de backend.
________________________________________
Tecnologias Utilizadas
•	Python 3.12
•	FastAPI
•	Uvicorn
•	SQLAlchemy
•	SQLite
•	Pydantic
•	Passlib (bcrypt)
•	Python-Jose (JWT)
________________________________________

Arquitetura do Projeto

A aplicação foi estruturada em camadas para facilitar manutenção e escalabilidade:
app/
├── main.py
├── database.py
├── models.py
├── schemas.py
├── auth.py
└── routes/
  └── user_routes.py
  
Responsabilidades
•	database.py → Configuração da conexão com o banco e criação da sessão.
•	models.py → Definição das entidades do banco de dados.
•	schemas.py → Validação e definição dos contratos da API.
•	auth.py → Regras de autenticação, hash de senha e geração de token.
•	routes/ → Definição das rotas e regras de negócio.
•	main.py → Inicialização da aplicação e registro das rotas.
________________________________________
Funcionalidades
•	Cadastro de usuário
•	Login com geração de token JWT
•	Listagem de usuários
•	Busca de usuário por ID
•	Atualização de usuário
•	Exclusão de usuário
•	Senhas armazenadas com hash bcrypt
________________________________________
Como Executar o Projeto
1. Clonar o repositório
git clone https://github.com/seu-usuario/seu-repositorio.git
cd seu-repositorio
2. Criar ambiente virtual
python -m venv venv
Windows:
venv\Scripts\activate
Linux/Mac:
source venv/bin/activate

4. Instalar dependências
pip install fastapi uvicorn sqlalchemy passlib[bcrypt] python-jose

5. Executar a aplicação
uvicorn app.main:app --reload
A aplicação estará disponível em:
http://127.0.0.1:8000
________________________________________
Documentação da API
A documentação interativa gerada automaticamente pode ser acessada em:
http://127.0.0.1:8000/docs
________________________________________
Autenticação
O endpoint de login retorna um access_token no formato JWT.
Esse token pode ser utilizado para autenticação via Bearer Token em rotas protegidas.
________________________________________
Possíveis Melhorias
•	Implementar proteção de rotas com validação de token
•	Adicionar refresh token
•	Implementar versionamento de API
•	Adicionar testes automatizados
•	Dockerizar a aplicação
•	Migrar para PostgreSQL
•	Utilizar Alembic para migrations
________________________________________
Objetivo do Projeto
Este projeto demonstra:
•	Organização em camadas
•	Separação entre modelo de banco e contrato da API
•	Uso de ORM
•	Implementação de autenticação com JWT
•	Aplicação de boas práticas em backend
Desenvolvido com foco em estudo e portfólio para backend júnior.
