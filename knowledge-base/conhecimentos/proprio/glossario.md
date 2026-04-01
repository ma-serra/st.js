---
titulo: Glossário de Termos de IA
tags: [#conhecimento, #proprio, #educacao, #multi-modelo, #estavel]
versao: 1.0.0
criado_em: 2026-03-21
atualizado_em: 2026-03-21
---

## Resumo

Glossário de termos técnicos utilizados em prompts, agentes e documentações desta base de conhecimento.

## Termos

### A

**Agente (Agent)**
Sistema de IA que usa um LLM como "cérebro" para planejar e executar tarefas de forma autônoma, usando ferramentas externas em ciclos iterativos.

**API (Application Programming Interface)**
Interface para comunicação entre sistemas. No contexto de LLMs, refere-se às APIs da OpenAI, Anthropic, Google, etc.

### C

**Chain-of-Thought (CoT)**
Técnica de prompting que instrui o modelo a raciocinar passo a passo antes de responder.

**Chunk**
Fragmento de texto criado ao dividir documentos longos para processamento em sistemas RAG.

**Context Window**
Limite máximo de tokens que um modelo pode processar em uma única interação.

### E

**Embedding**
Representação numérica (vetor) de texto que captura seu significado semântico, usada em sistemas de busca vetorial.

### F

**Few-Shot Learning**
Técnica onde o modelo aprende uma tarefa a partir de poucos exemplos fornecidos no prompt.

**Fine-Tuning**
Processo de retreinar um modelo pré-treinado com dados específicos de um domínio.

### G

**Grounding**
Processo de conectar o modelo a informações externas verificáveis para reduzir alucinações.

### H

**Hallucination (Alucinação)**
Quando um modelo gera informações falsas ou inexistentes com aparência de confiança.

### L

**LLM (Large Language Model)**
Modelo de linguagem de grande escala treinado em vastas quantidades de texto. Ex: GPT-4, Claude, Gemini.

**LangChain**
Framework Python/JavaScript para construir aplicações com LLMs, incluindo agentes, chains e RAG.

### P

**Prompt**
Texto de entrada fornecido a um modelo de linguagem para guiar sua resposta.

**Prompt Engineering**
Arte e ciência de criar prompts eficazes para obter melhores respostas de LLMs.

### R

**RAG (Retrieval-Augmented Generation)**
Técnica que combina busca em base de dados com geração de texto para respostas mais precisas e atualizadas.

**ReAct**
Padrão de agente que combina Raciocínio (Reasoning) e Ação (Acting) em ciclos iterativos.

### S

**Self-Consistency**
Técnica que gera múltiplas respostas independentes e seleciona a mais consistente por votação.

**Skill**
Capacidade modular e reutilizável que pode ser composta em prompts e agentes.

**System Prompt**
Instrução inicial fornecida ao modelo para definir seu papel, comportamento e restrições.

### T

**Temperature**
Parâmetro que controla a aleatoriedade das respostas (0 = determinístico, 2 = muito criativo).

**Token**
Unidade básica de texto processada por LLMs. Aproximadamente 0.75 palavras em inglês.

**Tool / Ferramenta**
Função externa que um agente pode chamar para realizar ações no mundo (busca, calculadora, API, etc.).

### Z

**Zero-Shot Learning**
Capacidade do modelo de realizar tarefas sem exemplos específicos no prompt.

## Referências

- [OpenAI Documentation](https://platform.openai.com/docs)
- [Anthropic Documentation](https://docs.anthropic.com)
- [Prompt Engineering Guide](https://www.promptingguide.ai)
- [LangChain Documentation](https://docs.langchain.com)
