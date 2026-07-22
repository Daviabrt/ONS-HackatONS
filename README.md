# ONS-HackatONS

Assistente inteligente para consulta e análise de dados do Operador Nacional do Sistema Elétrico (ONS), integrando dados públicos com IA generativa via Google Gemini.

---

## 📌 O que faz

O projeto acessa, organiza e disponibiliza os dados abertos do ONS (https://dados.ons.org.br/), permitindo que qualquer usuário faça perguntas em linguagem natural e obtenha respostas contextualizadas sobre o sistema elétrico brasileiro.

**Exemplo de perguntas:**
- "Qual foi a carga de energia no Sudeste no último mês?"
- "Como está a situação dos reservatórios das hidrelétricas?"
- "Qual a previsão de demanda para o próximo trimestre?"

---

## 🏗️ Arquitetura

┌─────────────────────────────────────────────────────────┐
│ Dados ONS (públicos) │
│ https://dados.ons.org.br/ │
└─────────────────────┬───────────────────────────────────┘
│
▼
┌─────────────────────────────────────────────────────────┐
│ Leitura e organização dos dados │
│ (AWS - armazenamento e processamento) │
└─────────────────────┬───────────────────────────────────┘
│
▼
┌─────────────────────────────────────────────────────────┐
│ Agente Inteligente (LangChain + Gemini) │
│ Interpreta perguntas e consulta os dados │
└─────────────────────┬───────────────────────────────────┘
│
▼
┌─────────────────────────────────────────────────────────┐
│ Interface interativa (Chatbot) │
│ Plataforma web amigável │
└─────────────────────────────────────────────────────────┘

---

## 🛠️ Tecnologias

- **LangChain** - Orquestração do agente de IA
- **Google Gemini** - Modelo de linguagem para compreensão e respostas
- **AWS (S3/Glue/Athena)** - Armazenamento e processamento dos dados
- **Frontend** - Interface interativa para chat
