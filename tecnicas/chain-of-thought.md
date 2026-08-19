# Chain-of-Thought (CoT) — Raciocínio passo a passo

> Faz o modelo **pensar antes de responder**: em vez de pular para a saída, ele expõe as etapas de raciocínio primeiro. Reduz drasticamente respostas rasas ou caóticas em tarefas complexas.

| | |
|---|---|
| **Tipo** | Técnica de raciocínio |
| **Melhor para** | Tarefas de alta complexidade: arquitetura de fluxos, decisões com trade-off, jornadas completas |
| **Combina bem com** | [CARE](../frameworks/01-ux-ui/CARE.md) · [C-C-E-R-A](../frameworks/01-ux-ui/C-C-E-R-A.md) · [CRISPE](../frameworks/02-gerais/CRISPE.md) |

---

## O que é

Você instrui o modelo a **decompor o problema em passos ordenados e resolvê-los na sequência**, só produzindo a resposta final depois de percorrer o raciocínio. É o antídoto contra o "salto para a conclusão", que em UX gera o vício de **telas soltas sem lógica de jornada** (*screen myopia*).

## Quando usar

- O resultado depende de uma **sequência lógica** (jornada, fluxo, arquitetura).
- Há **muitas variáveis** a considerar antes de decidir o layout/copy.
- Você quer **auditar o raciocínio** do modelo, não só o resultado.

## Como aplicar

Adicione ao seu prompt uma instrução explícita de etapas numeradas **antes** do entregável:

```text
Antes de detalhar a resposta final, siga estes passos de forma estrita:
1. [Análise do problema / fricções]
2. [Mapeamento da lógica / jornada]
3. [Dedução do mínimo necessário]
4. Só depois de concluir 1–3, produza [o entregável final].
```

## Exemplo (aplicado a UX)

> "Antes de estruturar as telas, (1) analise as 3 principais fricções cognitivas do usuário iniciante, (2) mapeie a transição lógica entre as 4 telas, (3) deduza a informação mínima de cada tela, (4) só então especifique o layout."

Isso aparece completo na receita [Arquitetura de fluxo de onboarding](../receitas/onboarding/arquitetura-fluxo-onboarding.md).

## Armadilhas

- **Passos vagos** produzem raciocínio vago. Seja específico no que cada etapa deve analisar.
- Se você **não exigir** que a resposta final venha só após os passos, o modelo pode ignorá-los.
- Combine com um **formato de saída** rígido para o raciocínio não virar texto solto.

---

📚 [← Índice](../README.md) · Relacionadas: [Decomposição / Step Zero](decomposicao-step-zero.md) · [Autocrítica](autocritica.md)
