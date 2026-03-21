---
titulo: RAG — Retrieval-Augmented Generation
tags: [#skill, #terceiros, #pesquisa, #extracao, #geracao, #langchain, #openai-api, #estavel]
modelo: Multi-modelo
versao: 1.0.0
fonte: "Lewis et al., 2020 — Retrieval-Augmented Generation for Knowledge-Intensive NLP Tasks"
licenca: "Apache 2.0"
criado_em: 2026-03-21
atualizado_em: 2026-03-21
---

## Descrição

Padrão de skill que combina busca em base de conhecimento externa com geração de texto, permitindo que o modelo responda com informações atualizadas e específicas do domínio.

## Entrada

- Pergunta do usuário
- Documentos/chunks recuperados da base de conhecimento

## Saída

Resposta baseada nos documentos recuperados, com citação das fontes.

## Implementação

```
Você é um assistente que responde perguntas com base nos documentos fornecidos.

Use APENAS as informações dos documentos abaixo para responder. Se a resposta não estiver nos documentos, diga "Não encontrei essa informação nos documentos disponíveis."

Documentos recuperados:
{{documentos}}

Pergunta: {{pergunta}}

Resposta (cite o documento de origem quando relevante):
```

## Como Usar

1. Implementar sistema de embeddings para sua base de conhecimento
2. Na query do usuário, recuperar os top-K chunks mais relevantes (similaridade coseno)
3. Injetar os chunks como `{{documentos}}`
4. O modelo gera a resposta baseada nesses chunks

## Implementação Técnica (Python + LangChain)

```python
from langchain.chains import RetrievalQA
from langchain.vectorstores import Chroma
from langchain.embeddings import OpenAIEmbeddings

vectorstore = Chroma(embedding_function=OpenAIEmbeddings())
qa_chain = RetrievalQA.from_chain_type(
    llm=llm,
    retriever=vectorstore.as_retriever(search_kwargs={"k": 4})
)
```

## Fonte

- Paper: [RAG for Knowledge-Intensive NLP Tasks](https://arxiv.org/abs/2005.11401)
- Autores: Patrick Lewis et al. (Facebook AI), 2020

## Notas

- Escolha embeddings adequados ao idioma (ex: `text-embedding-3-small` para multilíngue)
- Top-K entre 3 e 5 chunks geralmente dá bons resultados
- Implemente re-ranking para melhorar a qualidade da recuperação
