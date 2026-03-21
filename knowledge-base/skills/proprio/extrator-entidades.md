---
titulo: Extrator de Entidades
tags: [#skill, #proprio, #extracao, #classificacao, #analise, #multi-modelo, #estavel]
modelo: Multi-modelo
versao: 1.0.0
criado_em: 2026-03-21
atualizado_em: 2026-03-21
---

## Descrição

Extrai entidades nomeadas (pessoas, organizações, locais, datas, valores) de um texto e retorna em formato estruturado.

## Entrada

Texto livre em qualquer idioma.

## Saída

JSON com entidades classificadas por tipo.

## Implementação

```
Extraia todas as entidades do texto abaixo e classifique-as por tipo.

Tipos de entidade:
- PESSOA: nomes de pessoas
- ORGANIZACAO: empresas, instituições, órgãos
- LOCAL: países, cidades, endereços, regiões
- DATA: datas e períodos de tempo
- VALOR: valores monetários, percentuais, quantidades
- PRODUTO: nomes de produtos ou serviços
- OUTRO: outras entidades relevantes

Texto:
"""
{{texto}}
"""

Retorne APENAS um JSON válido com o seguinte formato:
{
  "entidades": [
    {"tipo": "PESSOA", "valor": "João Silva", "contexto": "trecho onde aparece"},
    {"tipo": "ORGANIZACAO", "valor": "Empresa X", "contexto": "trecho onde aparece"}
  ]
}
```

## Como Usar

Substitua `{{texto}}` pelo texto de entrada. A saída será um JSON que pode ser parseado programaticamente.

## Exemplos

**Entrada:**
> "A Apple anunciou hoje em Cupertino que Tim Cook apresentará o novo iPhone no dia 15 de setembro."

**Saída:**
```json
{
  "entidades": [
    {"tipo": "ORGANIZACAO", "valor": "Apple", "contexto": "A Apple anunciou"},
    {"tipo": "LOCAL", "valor": "Cupertino", "contexto": "hoje em Cupertino"},
    {"tipo": "PESSOA", "valor": "Tim Cook", "contexto": "que Tim Cook apresentará"},
    {"tipo": "PRODUTO", "valor": "iPhone", "contexto": "o novo iPhone"},
    {"tipo": "DATA", "valor": "15 de setembro", "contexto": "no dia 15 de setembro"}
  ]
}
```
