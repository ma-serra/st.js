---
titulo: Few-Shot Classifier
tags: [#prompt, #terceiros, #classificacao, #extracao, #multi-modelo, #estavel]
modelo: Multi-modelo
versao: 1.0.0
fonte: "Prompt Engineering Guide — promptingguide.ai"
licenca: "Uso livre / educacional"
criado_em: 2026-03-21
atualizado_em: 2026-03-21
---

## Descrição

Técnica de few-shot learning que fornece exemplos rotulados para guiar o modelo na classificação de novos itens sem fine-tuning.

## Caso de Uso

Use para classificar textos, sentimentos, intenções, categorias de suporte, etc.

## Prompt

```
Classifique o sentimento dos textos abaixo como: Positivo, Negativo ou Neutro.

Exemplos:
Texto: "O produto chegou rápido e em perfeito estado!" → Positivo
Texto: "Não gostei nada, veio com defeito." → Negativo
Texto: "O pedido foi entregue." → Neutro
Texto: "Atendimento razoável, poderia melhorar." → Neutro

Agora classifique:
Texto: "{{texto}}" →
```

## Variáveis

| Variável | Descrição | Exemplo |
|----------|-----------|---------|
| `{{texto}}` | Texto a ser classificado | `"Adorei a experiência de compra!"` |

## Exemplos de Saída

`Positivo`

## Personalização

Substitua os exemplos e os rótulos (`Positivo`, `Negativo`, `Neutro`) para adaptar a qualquer tarefa de classificação.

## Fonte

- [Prompt Engineering Guide](https://www.promptingguide.ai/techniques/fewshot)

## Notas

- Funciona bem mesmo em modelos menores
- Quanto mais exemplos de qualidade, melhor a precisão
