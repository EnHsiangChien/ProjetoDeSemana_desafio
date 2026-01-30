# 🏥 SmartSaúde SUS

![Status](https://img.shields.io/badge/status-MVP-blue)
![Academic](https://img.shields.io/badge/FECAP-Projeto%20Acadêmico-orange)
![License](https://img.shields.io/badge/license-CC%20BY%204.0-green)

## 📌 Instituição
**FECAP – Fundação de Comércio Álvares Penteado**  
🔗 https://www.fecap.br/

<p align="center">
  <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRhZPrRa89Kma0ZZogxm0pi-tCn_TLKeHGVxywp-LXAFGR3B1DPouAJYHgKZGV0XTEf4AE&usqp=CAU" alt="FECAP" width="300"/>
</p>

---

## 👥 Integrantes
- Eric de Lucas Silva  
- Stephanie Macedo da Silva  
- EnHsiang Chien  

---

## 🧠 Descrição do Projeto

O **SmartSaúde SUS** é uma plataforma inteligente de apoio ao atendimento do Sistema Único de Saúde (SUS), desenvolvida como um **MVP funcional** para projetos acadêmicos de curta duração.

O sistema tem como objetivo **auxiliar o cidadão no direcionamento para unidades de saúde**, reduzindo o tempo de espera e facilitando o acesso a informações essenciais, como:
- disponibilidade de unidades,
- tempo médio de atendimento,
- nível de lotação,
- disponibilidade de medicamentos.

A aplicação utiliza **triagem clínica simplificada**, **cálculo de viabilidade logística** e um **assistente virtual**, promovendo uma experiência mais rápida, acessível e organizada para o usuário.

---

## 🧩 Principais Funcionalidades

- 🔍 Busca por unidades de saúde (UPA / UBS)
- 🩺 Triagem rápida baseada em sintomas
- 🧭 Recomendação de unidades considerando distância e tempo de espera
- 💊 Consulta de medicamentos disponíveis por unidade
- 💬 Assistente virtual para apoio e orientação

> ⚠️ O sistema **não realiza diagnósticos médicos**, apenas apoio informacional e encaminhamento.

---

## 🛠️ Tecnologias Utilizadas

### Backend
- Python 3.10+
- FastAPI
- SQLAlchemy
- MySQL 8.0

### Frontend
- React.js
- Tailwind CSS
- Axios

### Outros
- Git & GitHub
- Postman (testes de API)

---

## 🗂️ Estrutura de Pastas

```text
smart-saude-sus/
│
├── backend/
│   ├── app/
│   │   ├── main.py                 # Entry point da API (FastAPI)
│   │   ├── config.py               # Configurações e variáveis de ambiente
│   │   ├── database.py             # Conexão com MySQL (SQLAlchemy)
│   │   │
│   │   ├── models/                 # Modelos ORM (Banco de Dados)
│   │   │   ├── unidade.py
│   │   │   ├── estoque.py
│   │   │   ├── logs_triagem.py
│   │   │   └── __init__.py
│   │   │
│   │   ├── schemas/                # DTOs e validações (Pydantic)
│   │   │   ├── chat.py
│   │   │   ├── triagem.py
│   │   │   └── __init__.py
│   │   │
│   │   ├── routers/                # Endpoints da API
│   │   │   ├── atendimento.py
│   │   │   ├── chat_ia.py
│   │   │   ├── unidades.py
│   │   │   ├── roteamento.py
│   │   │   └── __init__.py
│   │   │
│   │   ├── services/               # Lógica de negócio
│   │   │   ├── manchester.py       # Algoritmo de triagem
│   │   │   ├── roteamento.py       # Cálculo de score de viabilidade
│   │   │   ├── ai_engine.py        # IA com injeção de contexto (RAG)
│   │   │   ├── Groq_client.py      # Cliente de IA Generativa
│   │   │   ├── ai/                 # Recursos auxiliares de IA
│   │   │   └── __init__.py
│   │   │
│   │   └── utils/                  # Utilitários
│   │       ├── logging_middleware.py
│   │       └── __init__.py
│   │
│   ├── requirements.txt            # Dependências do backend
│  └── __init__.py
│ 
├── docs
│   └── init.sql
│ 
├── frontend/
│   ├── index.html
│   ├── package.json
│   ├── package-lock.json
│   ├── vite.config.ts
│   ├── eslint.config.js
│   ├── tsconfig.json
│   ├── tsconfig.app.json
│   ├── tsconfig.node.json
│   ├── public/
│   ├── src/                        # Código-fonte React
│   └── README.md
│
├── docs/
│   └── init.sql                    # Script inicial do banco de dados
│
└── README.md
