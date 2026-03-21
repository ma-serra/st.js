# 📚 Base de Conhecimento — st.js

Base centralizada de **prompts**, **agentes**, **skills** e **conhecimentos gerais** para conectar com modelos de IA.

---

## 🗂️ Estrutura

```
knowledge-base/
├── tags.md                    # Lista mestre de tags
├── prompts/
│   ├── README.md
│   ├── proprio/               # Prompts criados/customizados pelo dono
│   └── terceiros/             # Prompts de fontes externas
├── agentes/
│   ├── README.md
│   ├── proprio/               # Agentes próprios
│   └── terceiros/             # Agentes de terceiros
├── skills/
│   ├── README.md
│   ├── proprio/               # Skills próprias
│   └── terceiros/             # Skills de terceiros
└── conhecimentos/
    ├── README.md
    ├── proprio/               # Conhecimento próprio / interno
    └── terceiros/             # Conhecimento externo / documentações
```

---

## 📖 Índice

| Seção | Descrição | Próprio | Terceiros |
|-------|-----------|---------|-----------|
| [Prompts](./prompts/README.md) | Prompts de texto para modelos de linguagem | [→](./prompts/proprio/) | [→](./prompts/terceiros/) |
| [Agentes](./agentes/README.md) | Agentes autônomos e semi-autônomos | [→](./agentes/proprio/) | [→](./agentes/terceiros/) |
| [Skills](./skills/README.md) | Habilidades e capacidades reutilizáveis | [→](./skills/proprio/) | [→](./skills/terceiros/) |
| [Conhecimentos](./conhecimentos/README.md) | Base de contexto e conhecimento geral | [→](./conhecimentos/proprio/) | [→](./conhecimentos/terceiros/) |

---

## 🏷️ Tags

Veja a [lista completa de tags](./tags.md) para filtrar e organizar os itens por:
- **Categoria**: `#prompt`, `#agente`, `#skill`, `#conhecimento`
- **Origem**: `#proprio`, `#terceiros`
- **Função**: `#geracao`, `#resumo`, `#traducao`, `#qa`, `#analise`, etc.
- **Tema**: `#codigo`, `#escrita`, `#negocios`, `#educacao`, etc.
- **Modelo**: `#gpt`, `#claude`, `#gemini`, `#llama`, etc.
- **Status**: `#estavel`, `#experimental`, `#rascunho`

---

## ➕ Como Contribuir

1. Escolha a seção adequada (`prompts`, `agentes`, `skills` ou `conhecimentos`)
2. Escolha a subpasta (`proprio` ou `terceiros`)
3. Crie um arquivo `.md` com o nome descritivo do item
4. Adicione o bloco de metadados com as tags no topo:

```yaml
---
titulo: Meu Novo Prompt
tags: [#prompt, #proprio, #codigo, #geracao, #gpt, #estavel]
modelo: GPT-4
versao: 1.0.0
criado_em: AAAA-MM-DD
atualizado_em: AAAA-MM-DD
---
```

5. Documente o item seguindo o template de cada seção
