---
titulo: Gerador de Código
tags: [#prompt, #proprio, #codigo, #geracao, #gpt, #estavel]
modelo: GPT-4
versao: 1.0.0
criado_em: 2026-03-21
atualizado_em: 2026-03-21
---

## Descrição

Gera código limpo e comentado em qualquer linguagem de programação a partir de uma descrição em linguagem natural.

## Caso de Uso

Use quando precisar criar funções, classes, scripts ou módulos a partir de uma descrição funcional.

## Prompt

```
Você é um engenheiro de software sênior especialista em {{linguagem}}.

Sua tarefa é escrever código de alta qualidade com base na seguinte descrição:

{{descricao}}

Requisitos:
- Código limpo, legível e bem estruturado
- Comentários explicativos nas partes complexas
- Tratamento de erros adequado
- Siga as melhores práticas da linguagem {{linguagem}}
- Se aplicável, inclua exemplos de uso

Responda apenas com o código e os comentários necessários.
```

## Variáveis

| Variável | Descrição | Exemplo |
|----------|-----------|---------|
| `{{linguagem}}` | Linguagem de programação desejada | `TypeScript`, `Python`, `Go` |
| `{{descricao}}` | Descrição funcional do que deve ser gerado | `"Função que valida um CPF brasileiro"` |

## Exemplos de Saída

Código TypeScript validando um CPF com comentários e casos de erro tratados.

## Notas

- Funciona melhor com GPT-4 ou Claude 3 Opus
- Para saídas muito longas, divida a tarefa em partes menores
