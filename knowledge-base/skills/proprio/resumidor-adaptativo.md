---
titulo: Resumidor Adaptativo
tags: [#skill, #proprio, #resumo, #escrita, #analise, #multi-modelo, #estavel]
modelo: Multi-modelo
versao: 1.0.0
criado_em: 2026-03-21
atualizado_em: 2026-03-21
---

## Descrição

Gera resumos de textos com controle preciso do tamanho e nível de detalhe, adaptando-se ao público-alvo.

## Entrada

- Texto a ser resumido
- Tamanho desejado (em palavras ou parágrafos)
- Público-alvo
- Nível de detalhe (executivo, técnico, educacional)

## Saída

Resumo no tamanho e formato especificados.

## Implementação

```
Resuma o texto abaixo com as seguintes especificações:

- Tamanho: {{tamanho}}
- Público-alvo: {{publico}}
- Nível de detalhe: {{nivel}} (executivo / técnico / educacional)
- Idioma: {{idioma}}

Diretrizes:
- Preserve as informações mais importantes
- Mantenha a ordem lógica das ideias
- Use linguagem adequada ao público-alvo
- Não inclua opiniões não presentes no original

Texto:
"""
{{texto}}
"""
```

## Como Usar

Configure os parâmetros conforme necessidade e substitua `{{texto}}` pelo conteúdo a resumir.

## Exemplos

**Configuração:**
- Tamanho: 3 frases
- Público: líderes executivos
- Nível: executivo
- Idioma: Português

**Entrada:** Artigo técnico de 2000 palavras sobre RAG

**Saída:** 
> "RAG (Retrieval-Augmented Generation) é uma técnica que melhora respostas de IA ao buscar informações relevantes em bases de dados antes de gerar respostas. Diferente do fine-tuning, não requer retreinamento do modelo, reduzindo custos em até 90%. Empresas que adotaram RAG reportam aumento de 40% na precisão das respostas de seus assistentes virtuais."

## Notas

- Para textos muito longos, use em conjunto com chunking
- Nível "executivo": foca em impacto e decisões
- Nível "técnico": inclui detalhes de implementação
- Nível "educacional": usa analogias e explica termos
