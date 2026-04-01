---
titulo: Chain-of-Thought (CoT)
tags: [#prompt, #terceiros, #qa, #analise, #raciocinio, #multi-modelo, #estavel]
modelo: Multi-modelo
versao: 1.0.0
fonte: "Wei et al., 2022 — Chain-of-Thought Prompting Elicits Reasoning in Large Language Models"
licenca: "Uso livre / pesquisa"
criado_em: 2026-03-21
atualizado_em: 2026-03-21
---

## Descrição

Técnica de prompting que instrui o modelo a raciocinar passo a passo antes de dar a resposta final, aumentando a precisão em tarefas de raciocínio lógico e matemático.

## Caso de Uso

Use para problemas que exigem raciocínio multi-etapa: matemática, lógica, resolução de problemas, análise de cenários.

## Prompt

```
Resolva o seguinte problema passo a passo, mostrando todo o raciocínio antes de chegar à resposta final.

Problema: {{problema}}

Raciocínio passo a passo:
```

## Variáveis

| Variável | Descrição | Exemplo |
|----------|-----------|---------|
| `{{problema}}` | O problema ou questão a ser resolvido | `"Se João tem 3x mais maçãs que Maria..."` |

## Exemplos de Saída

O modelo apresenta cada etapa do raciocínio numerada, chegando à conclusão de forma transparente.

## Fonte

- Paper original: [Chain-of-Thought Prompting Elicits Reasoning in LLMs](https://arxiv.org/abs/2201.11903)
- Autores: Wei et al. (Google Brain), 2022

## Notas

- Mais eficaz em modelos grandes (GPT-4, Claude 3, Gemini Ultra)
- Adicione "Pense devagar e com cuidado" para reforçar o comportamento
