---
titulo: Guia de Prompt Engineering
tags: [#conhecimento, #terceiros, #educacao, #multi-modelo, #estavel]
versao: 1.0.0
fonte: "Prompt Engineering Guide — promptingguide.ai (Dair AI)"
licenca: "MIT"
criado_em: 2026-03-21
atualizado_em: 2026-03-21
---

## Resumo

Resumo das principais técnicas de prompt engineering documentadas no Prompt Engineering Guide, um dos recursos mais completos da comunidade sobre o tema.

## Técnicas Principais

### 1. Zero-Shot Prompting
Pedir ao modelo que realize uma tarefa sem fornecer exemplos.
```
Classifique o sentimento: "Amei o produto!"
```

### 2. Few-Shot Prompting
Fornecer exemplos antes da tarefa principal para guiar o modelo.
```
Positivo: "Produto excelente!"
Negativo: "Muito ruim."
Classifique: "Chegou rápido."
```

### 3. Chain-of-Thought (CoT)
Instrui o modelo a raciocinar passo a passo.
```
Responda passo a passo: Se João tem 5 maçãs...
```

### 4. Zero-Shot CoT
Adiciona "Vamos pensar passo a passo" ao prompt sem exemplos.
```
Vamos pensar passo a passo. Se João tem 5 maçãs...
```

### 5. Self-Consistency
Gerar múltiplas respostas e selecionar a mais consistente (ver skill dedicada).

### 6. Generated Knowledge Prompting
Solicitar ao modelo que gere conhecimento relevante antes de responder.
```
Gere fatos sobre fotossíntese. Agora, com base nisso, explique...
```

### 7. ReAct
Combinação de raciocínio e ação em ciclos (ver agente dedicado).

### 8. Directional Stimulus Prompting
Fornecer uma dica ou palavra-chave para guiar a resposta.
```
Descreva a fotossíntese. Dica: use os termos clorofila, luz solar e glicose.
```

### 9. Tree of Thoughts (ToT)
Explorar múltiplos caminhos de raciocínio em árvore.

### 10. Retrieval-Augmented Generation (RAG)
Combinar busca em base de dados com geração (ver skill dedicada).

## Boas Práticas

1. **Seja específico**: Prompts vagos geram respostas vagas
2. **Defina o papel**: "Você é um especialista em X"
3. **Formato de saída**: Especifique como a resposta deve ser formatada
4. **Exemplos ajudam**: Few-shot > zero-shot na maioria dos casos
5. **Itere**: Prompts são melhorados progressivamente
6. **Temperature**: Use 0 para tarefas factuais, >0 para criatividade
7. **Evite negações**: Prefira "use linguagem formal" a "não use linguagem informal"

## Anti-Padrões

- Prompts ambíguos sem contexto suficiente
- Solicitar múltiplas tarefas diferentes sem estrutura
- Não especificar o idioma da resposta quando necessário
- Instruções contraditórias no mesmo prompt

## Fonte

- [Prompt Engineering Guide](https://www.promptingguide.ai) — Dair AI
- Licença: MIT
- Repositório: [github.com/dair-ai/Prompt-Engineering-Guide](https://github.com/dair-ai/Prompt-Engineering-Guide)
