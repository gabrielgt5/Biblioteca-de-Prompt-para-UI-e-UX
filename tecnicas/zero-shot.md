# Zero-Shot — Instrução direta, sem exemplos

> O modelo executa a tarefa **apenas com a instrução**, sem exemplos resolvidos. É o modo mais rápido e enxuto — ideal quando a tarefa é comum e não ambígua.

| | |
|---|---|
| **Tipo** | Técnica de contexto |
| **Melhor para** | Tarefas simples, comuns e de baixa ambiguidade; primeiras iterações rápidas |
| **Combina bem com** | [ICE](../frameworks/01-ux-ui/ICE.md) · [RACE](../frameworks/02-gerais/RACE.md) |

---

## O que é

Você dá a instrução e confia no conhecimento prévio do modelo, **sem demonstrar** o formato. É o oposto do [Few-Shot](few-shot.md). A maioria dos prompts do dia a dia começa aqui.

## Quando usar

- A tarefa é **familiar** e o formato desejado é **óbvio** ou pouco crítico.
- Você quer **velocidade** e vai refinar depois com [prompting iterativo](prompting-iterativo.md).
- O custo de um pequeno desvio de formato é baixo.

## Como aplicar

```text
[Papel] + [ação clara] + [formato desejado em uma frase].
Ex.: "Aja como UX Writer e escreva 5 opções de título para um empty state,
cada uma com no máximo 4 palavras."
```

## Quando NÃO usar

- Sintaxe técnica complexa ou terminologia interna → use [Few-Shot](few-shot.md).
- Raciocínio de jornada/arquitetura → use [Chain-of-Thought](chain-of-thought.md).
- Consistência absoluta entre muitos itens → use [Few-Shot](few-shot.md).

## Armadilhas

- Sem exemplo, o modelo **assume um formato** — que pode não ser o seu.
- Em tarefas críticas, a economia de esforço vira retrabalho. Suba de técnica cedo.

---

[← Índice](../README.md) · Relacionadas: [Few-Shot](few-shot.md) · [Prompting iterativo](prompting-iterativo.md)
