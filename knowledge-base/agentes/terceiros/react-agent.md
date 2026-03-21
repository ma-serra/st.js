---
titulo: ReAct Agent (Reasoning + Acting)
tags: [#agente, #terceiros, #pesquisa, #automacao, #planejamento, #langchain, #multi-modelo, #estavel]
modelo: Multi-modelo
versao: 1.0.0
fonte: "Yao et al., 2022 — ReAct: Synergizing Reasoning and Acting in Language Models"
licenca: "Apache 2.0"
criado_em: 2026-03-21
atualizado_em: 2026-03-21
---

## Descrição

Padrão de agente que combina raciocínio (Thought) e ação (Action) em ciclos iterativos até resolver a tarefa. Base de muitos frameworks modernos como LangChain e LlamaIndex.

## Objetivo

Resolver tarefas complexas que requerem múltiplas etapas de raciocínio e uso de ferramentas externas.

## System Prompt

```
Responda as seguintes perguntas da melhor forma possível. Você tem acesso às seguintes ferramentas:

{{ferramentas}}

Use o seguinte formato:

Pergunta: a pergunta que você deve responder
Pensamento: você deve sempre pensar sobre o que fazer
Ação: a ação a ser tomada, deve ser uma das [{{lista_ferramentas}}]
Entrada da Ação: a entrada para a ação
Observação: o resultado da ação
... (este ciclo Pensamento/Ação/Entrada/Observação pode se repetir N vezes)
Pensamento: Agora sei a resposta final
Resposta Final: a resposta final à pergunta original

Comece!

Pergunta: {{pergunta}}
Pensamento:
```

## Variáveis

| Variável | Descrição | Exemplo |
|----------|-----------|---------|
| `{{ferramentas}}` | Descrição das ferramentas disponíveis | `"Busca: pesquisa na web. Calculadora: faz cálculos."` |
| `{{lista_ferramentas}}` | Nomes das ferramentas | `"Busca, Calculadora"` |
| `{{pergunta}}` | A pergunta ou tarefa para o agente | `"Qual é a capital da França e sua população?"` |

## Ferramentas / Skills Necessárias

- Qualquer ferramenta que possa ser descrita e chamada pelo modelo (busca, calculadora, banco de dados, APIs)

## Fluxo de Funcionamento

1. Agente recebe pergunta
2. Ciclo: Pensamento → Ação → Observação
3. Agente determina quando tem informação suficiente
4. Agente fornece resposta final

## Fonte

- Paper: [ReAct: Synergizing Reasoning and Acting in LLMs](https://arxiv.org/abs/2210.03629)
- Autores: Shunyu Yao et al. (Princeton / Google Brain), 2022
- Implementação LangChain: [docs.langchain.com](https://docs.langchain.com/docs/components/agents/agent-types/react)

## Notas

- Funciona melhor com GPT-4, Claude 3+
- Implementação nativa disponível em LangChain e LlamaIndex
