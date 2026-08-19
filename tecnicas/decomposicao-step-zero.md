# Decomposição / "Step Zero" — Pensar a jornada antes das telas

> Uma disciplina de raciocínio: **antes de detalhar qualquer elemento visual**, obrigue o modelo a resolver a lógica macro (jornada, arquitetura, objetivos). O "passo zero" que impede o vício de gerar telas soltas.

| | |
|---|---|
| **Tipo** | Técnica de raciocínio (parente do [Chain-of-Thought](chain-of-thought.md)) |
| **Melhor para** | Fluxos multi-tela, arquitetura de informação, jornadas ponta a ponta |
| **Combina bem com** | [CARE](../frameworks/01-ux-ui/CARE.md) · [RTCF](../frameworks/01-ux-ui/RTCF.md) |

---

## O que é

*Screen myopia* é a tendência da IA (e de designers apressados) de projetar **telas isoladas** sem conexão de fluxo. O "Step Zero" combate isso inserindo uma etapa obrigatória de raciocínio de alto nível **antes** do detalhamento:

> Primeiro a **jornada** e os **objetivos de cada etapa**; só depois os **componentes** de cada tela.

Enquanto o [Chain-of-Thought](chain-of-thought.md) é a técnica geral de "pensar em passos", a Decomposição/Step Zero é sua aplicação específica a **problemas de fluxo e arquitetura**.

## Quando usar

- O entregável tem **mais de uma tela** ou etapas encadeadas.
- Existe risco de o modelo detalhar botões e cores antes de entender a **lógica da jornada**.
- Você quer que cada tela tenha um **objetivo claro** dentro do todo.

## Como aplicar

```text
Passo 0 (antes de qualquer layout):
- Mapeie a jornada completa: [Etapa 1 → Etapa 2 → Etapa 3 → …]
- Para cada etapa, defina o objetivo único e a informação mínima necessária.

Só depois de concluir o Passo 0, detalhe os componentes de cada tela.
```

## Exemplo (aplicado a UX)

No onboarding financeiro: o modelo primeiro mapeia `Boas-vindas → Verificação → Configuração → 1º depósito`, define o objetivo de cada tela e só então especifica os componentes. Veja [Arquitetura de fluxo de onboarding](../receitas/onboarding/arquitetura-fluxo-onboarding.md).

## Armadilhas

- Não deixe o "Passo 0" **opcional** — deixe explícito que o detalhamento só vem depois.
- Peça a **transição lógica entre etapas**, não só uma lista de telas.

---

📚 [← Índice](../README.md) · Relacionadas: [Chain-of-Thought](chain-of-thought.md) · [CARE](../frameworks/01-ux-ui/CARE.md)
