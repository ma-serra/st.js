---
titulo: Contexto do Projeto
tags: [#conhecimento, #proprio, #negocios, #produto, #estavel]
versao: 1.0.0
criado_em: 2026-03-21
atualizado_em: 2026-04-01
---

## Resumo

**st.js** é uma base centralizada de prompts, agentes, skills e conhecimentos gerais para conectar com modelos de IA. O repositório organiza esses recursos por categoria e origem (próprio vs. terceiros), com um sistema de tags para facilitar busca e reuso.

## Contexto / Background

O repositório surgiu da necessidade de centralizar e organizar recursos de IA de forma reutilizável e navegável. Em vez de manter prompts e configurações espalhados, o st.js oferece uma estrutura padronizada com metadados YAML, tags e templates para cada tipo de recurso.

## Estado Atual

### O que está pronto

**Prompts (próprios):**
- `gerador-codigo.md` — Geração de código em qualquer linguagem
- `revisor-texto.md` — Revisão e melhoria de textos
- `assistente-produto.md` — Assistente focado em produto e documentação

**Prompts (terceiros):**
- `chain-of-thought.md` — Técnica de raciocínio passo a passo
- `few-shot-classifier.md` — Classificação com exemplos

**Agentes (próprios):**
- `agente-dev.md` — Co-piloto de engenharia de software sênior
- `agente-pesquisa.md` — Agente de pesquisa e síntese de informação

**Agentes (terceiros):**
- `react-agent.md` — Padrão ReAct (Reason + Act)

**Skills (próprias):**
- `extrator-entidades.md` — Extração de entidades nomeadas
- `formatador-json.md` — Geração de estrutura JSON
- `resumidor-adaptativo.md` — Sumarização adaptativa com consciência de contexto

**Skills (terceiros):**
- `rag-retrieval.md` — Recuperação aumentada por geração (RAG) com LangChain
- `self-consistency.md` — Técnica de auto-consistência

**Conhecimentos (próprios):**
- `contexto-projeto.md` — Este documento
- `glossario.md` — 25+ termos de IA/LLM definidos em português

**Conhecimentos (terceiros):**
- `guia-prompt-engineering.md` — Trechos do Prompt Engineering Guide
- `modelos-disponiveis.md` — Comparativo de modelos disponíveis

**Infraestrutura:**
- `tags.md` — Lista mestre de 50+ tags em 6 dimensões (categoria, origem, função, tema, modelo, status)
- READMEs em todas as pastas com índice e templates de contribuição

## Objetivos do Projeto

- [x] Criar uma biblioteca reutilizável de prompts testados e documentados
- [x] Documentar agentes autônomos e semi-autônomos prontos para uso
- [x] Catalogar skills modulares combináveis
- [x] Manter uma base de conhecimento contextual para RAG e system prompts
- [ ] Expandir com novos prompts, agentes e skills conforme necessidade
- [ ] Testar e promover itens de `#experimental` e `#rascunho` para `#estavel`

## Público-Alvo

- Desenvolvedores que trabalham com LLMs
- Times de produto que integram IA em seus fluxos
- Pesquisadores que testam capacidades de modelos

## Stack / Ferramentas

- Modelos: GPT-4, Claude 3, Gemini, Llama, Mistral
- Frameworks: LangChain, LlamaIndex
- Formato: Markdown com metadados YAML

## Convenções do Projeto

- Todos os arquivos usam metadados YAML no topo
- Tags seguem o padrão definido em `/knowledge-base/tags.md`
- Prompts são documentados com variáveis no formato `{{variavel}}`
- Organização por origem: `proprio/` vs. `terceiros/`
- Itens de terceiros obrigatoriamente incluem campo `fonte` nos metadados

## Pontos-Chave

- Organização por origem: próprio vs. terceiros
- Tagging sistemático para fácil busca e filtro
- Templates padronizados por categoria
