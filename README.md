# 🧠 IA para Leitura de Documentos com Chat Interativo

Este projeto é uma aplicação em Python que treina uma Inteligência Artificial para **compreender documentos** e responder perguntas com base no conteúdo aprendido, através de um **chat interativo**. A IA utiliza técnicas de NLP, embeddings vetoriais e memória contextual para oferecer respostas precisas e relevantes a partir dos documentos fornecidos.

## ✨ Funcionalidades

- 📄 Treinamento de IA com documentos PDF ou texto;
- 💬 Interface de chat com respostas contextuais inteligentes;
- 🧠 Vetorização semântica com FAISS + Langchain + OpenAI 3.5;
- 🗓️ Agendamento e processamento assíncrono com Django Q e APScheduler;
- 🔐 Controle de usuários e permissões com Django Role Permissions.

## 🧪 Tecnologias e Bibliotecas

Principais bibliotecas utilizadas:

- **Framework:** Django 5.2.1
- **IA / NLP:** Langchain, OpenAI, FAISS, Langsmith, Tiktoken
- **Vetorização e busca semântica:** FAISS
- **Processamento de documentos:** PyPDF, BeautifulSoup4
- **Execução assíncrona:** Django-Q2, APScheduler
- **Comunicação:** HTTPX, SSE, Aiohttp
- **ORM e Banco de Dados:** Django ORM, SQLAlchemy
- **Outras:** Pydantic, Redis, Python Dotenv, Marshmallow

## 🚀 Como rodar o projeto

```bash
# Clone o repositório
git clone https://github.com/seu-usuario/seu-repo.git
cd seu-repo

# Crie e ative o ambiente virtual
python -m venv venv

# Linux:
source venv/bin/activate

# Windows:
venv\Scripts\activate

# Instale as dependências
pip install -r requirements.txt

# Crie o arquivo .env e adicione a variável OPENAI_API_KEY e seu valor
echo "OPENAI_API_KEY=sua-chave-aqui" > .env

# Realize as migrações do Django
python manage.py migrate

# Crie um superusuário
python manage.py createsuperuser

# Rode o servidor de desenvolvimento
python manage.py runserver

# Rode o worker de tarefas
python manage.py qcluster

# Acesse o painel de login para autenticar com o usuário cadastrado
http://localhost:8000/usuarios/login/

# Envie um documento (ex: Perceptron.pdf) para treinar a IA na seguinte rota
http://localhost:8000/oraculo/treinar_ia

# Acesse o chat e interaja com o modelo treinado
http://localhost:8000/oraculo/chat
```