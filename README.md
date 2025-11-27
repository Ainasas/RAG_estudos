# RAG com LLM pequeno

Este projeto demonstra a arquitetura **Retrieval-Augmented Generation (RAG)** para permitir que um LLM responda a perguntas baseadas **exclusivamente** em uma base de dados externa e específica.

O objetivo foi aprender os conceitos chaves e superar o problema de **alucinação** e a limitação de **conhecimento estático** dos LLMs com recursos de hardware limitados (utilizando apenas Colab).

### 🧠 Conceitos Estudados

O sistema RAG é composto por três fases lógicas integradas:

| Fase | Função no Projeto | Conceito Aplicado | Ferramentas Utilizadas |
| :---: | :--- | :---: | :---: |
| **1. Indexação** | Transforma documentos de texto em vetores numéricos. | **Word Embeddings** | Sentence Transformers (MiniLM) |
| **2. Recuperação** | Encontra os trechos de conhecimento mais semanticamente relevantes para a pergunta do usuário. | **Similaridade Vetorial** | FAISS (Facebook AI Similarity Search) |
| **3. Geração** | Sintetiza os trechos recuperados em uma resposta coerente e natural. | **Prompt Engineering** | Flan-T5-base (Hugging Face) |

### ❗Resultados interessantes
- Foi preciso um refinamento por prompt bruto e uso de um LLM relativamente mais complexo como o Fla-T5 para conseguir uma resposta "Ok"
- O modelo se mostrou com dificuldades para criar uma resposta própria baseada no contexto adquirido no index
- A falta de "Pensamento" único do LLM abre fronteiras para o uso de "Attention" para gerar respostas com valor
