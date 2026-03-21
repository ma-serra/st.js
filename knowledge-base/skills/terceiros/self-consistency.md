---
titulo: Self-Consistency (Auto-Consistência)
tags: [#skill, #terceiros, #qa, #analise, #avaliacao, #multi-modelo, #estavel]
modelo: Multi-modelo
versao: 1.0.0
fonte: "Wang et al., 2022 — Self-Consistency Improves Chain of Thought Reasoning in LLMs"
licenca: "Uso livre / pesquisa"
criado_em: 2026-03-21
atualizado_em: 2026-03-21
---

## Descrição

Técnica que aumenta a precisão de modelos gerando múltiplas respostas independentes e selecionando a mais consistente (por votação majoritária ou análise).

## Entrada

- Uma pergunta ou problema
- Número de amostras desejadas (recomendado: 5-10)

## Saída

A resposta mais consistente entre as amostras geradas.

## Implementação

**Passo 1 — Gerar N respostas independentes:**
```
[Use o prompt de Chain-of-Thought N vezes com temperatura > 0]
Resolva passo a passo: {{problema}}
```

**Passo 2 — Agregar respostas:**
```
Foram geradas as seguintes respostas independentes para o problema:

{{lista_respostas}}

Analise as respostas acima e:
1. Identifique qual resposta aparece com mais frequência ou é mais consistente
2. Explique por que ela é a mais confiável
3. Forneça a resposta final consolidada
```

## Como Usar

1. Execute o mesmo prompt N vezes com `temperature` entre 0.5 e 1.0
2. Colete as respostas
3. Use o Passo 2 para agregar (ou faça votação programática)

## Implementação Técnica

```python
import openai
from collections import Counter

def self_consistency(prompt, n=7, temperature=0.7):
    respostas = []
    for _ in range(n):
        r = openai.chat.completions.create(
            model="gpt-4",
            messages=[{"role": "user", "content": prompt}],
            temperature=temperature
        )
        respostas.append(r.choices[0].message.content)
    
    # Votação majoritária (para respostas curtas/categóricas)
    return Counter(respostas).most_common(1)[0][0]
```

## Fonte

- Paper: [Self-Consistency Improves CoT Reasoning](https://arxiv.org/abs/2203.11171)
- Autores: Xuezhi Wang et al. (Google Brain), 2022

## Notas

- Aumenta custo proporcionalmente a N (use com moderação em produção)
- Mais eficaz para problemas com resposta discreta (matemática, lógica)
- Para respostas abertas, use o Passo 2 de agregação com LLM
