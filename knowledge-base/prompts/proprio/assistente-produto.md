---
titulo: Assistente de Produto
tags: [#prompt, #proprio, #produto, #planejamento, #negocios, #gpt, #experimental]
modelo: GPT-4
versao: 0.9.0
criado_em: 2026-03-21
atualizado_em: 2026-03-21
---

## Descrição

Auxilia na criação de product briefs, definição de épicos, user stories e critérios de aceite.

## Caso de Uso

Use para estruturar funcionalidades de produto, escrever histórias de usuário e planejar sprints.

## Prompt

```
Você é um Product Manager experiente com background em metodologias ágeis.

Seu objetivo é ajudar a estruturar a seguinte funcionalidade de produto:

Funcionalidade: {{funcionalidade}}
Contexto do produto: {{contexto}}
Usuário alvo: {{usuario}}

Por favor, gere:

1. **Product Brief** (máximo 3 parágrafos)
2. **Épico**: título e descrição de alto nível
3. **User Stories** (mínimo 3):
   - Formato: "Como {{usuario}}, quero {{acao}}, para que {{beneficio}}"
4. **Critérios de Aceite** para cada user story
5. **Riscos e Dependências** identificados
```

## Variáveis

| Variável | Descrição | Exemplo |
|----------|-----------|---------|
| `{{funcionalidade}}` | Nome e descrição da funcionalidade | `"Sistema de notificações push"` |
| `{{contexto}}` | Contexto geral do produto | `"App de e-commerce B2C"` |
| `{{usuario}}` | Perfil do usuário alvo | `"comprador recorrente"` |

## Exemplos de Saída

Brief estruturado com épico, 3+ user stories e critérios de aceite detalhados.

## Notas

- Em fase experimental — outputs podem precisar de refinamento
- Funciona melhor com GPT-4 Turbo
