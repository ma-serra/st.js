---
titulo: Formatador JSON
tags: [#skill, #proprio, #extracao, #codigo, #automacao, #multi-modelo, #estavel]
modelo: Multi-modelo
versao: 1.0.0
criado_em: 2026-03-21
atualizado_em: 2026-03-21
---

## Descrição

Instrui o modelo a sempre retornar respostas em JSON válido com um schema predefinido. Útil para integração com APIs e pipelines de automação.

## Entrada

Qualquer instrução + schema JSON desejado.

## Saída

JSON válido conforme o schema fornecido.

## Implementação

```
Responda à seguinte solicitação retornando APENAS um JSON válido, sem nenhum texto adicional, markdown ou explicação.

Schema esperado:
{{schema}}

Solicitação:
{{instrucao}}

Responda apenas com o JSON:
```

## Como Usar

1. Defina o `{{schema}}` com o formato JSON esperado (pode usar JSON Schema ou um exemplo comentado)
2. Forneça a `{{instrucao}}` com o que deve ser gerado
3. Parse a resposta diretamente como JSON

## Exemplos

**Schema:**
```json
{
  "titulo": "string",
  "resumo": "string (max 2 frases)",
  "palavras_chave": ["string"],
  "sentimento": "positivo | negativo | neutro"
}
```

**Instrução:** `Analise este review: "Produto excelente, chegou antes do prazo e funcionou perfeitamente!"`

**Saída:**
```json
{
  "titulo": "Review positivo de produto",
  "resumo": "O cliente elogiou a qualidade do produto e a rapidez na entrega. Experiência muito positiva.",
  "palavras_chave": ["produto", "entrega", "qualidade", "prazo"],
  "sentimento": "positivo"
}
```

## Notas

- Use `response_format: { type: "json_object" }` na API da OpenAI para garantir JSON válido
- Com Claude, adicione "Responda SOMENTE com JSON" no início do system prompt
