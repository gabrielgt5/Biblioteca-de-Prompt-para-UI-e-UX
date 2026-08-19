# RTCF — Role, Task, Context, Format

> Muito usado para gerar **interfaces de alta fidelidade** e **código semântico**, evitando o problema de *screen myopia* (telas isoladas, sem conexão de fluxo).

| | |
|---|---|
| **Categoria** | UX/UI · Design de alta fidelidade & Handoff |
| **Melhor para** | Descrever componentes complexos, gerar telas para desenvolvimento, especificar código React / Auto Layout de Figma |
| **Nível** | Intermediário / Avançado |

---

## Quando usar

Use o RTCF quando o resultado é **executável** — uma tela, um componente, um trecho de código — e precisa se encaixar num ecossistema existente (design tokens, navegação, padrões do produto). O **Format** explícito é o que garante o handoff limpo.

## Anatomia

| Componente | O que é | Pergunta-guia |
|---|---|---|
| **R — Role** (Papel) | Ancoragem mental da IA como especialista. | Que especialista produziria isto? |
| **T — Task** (Tarefa) | O que deve ser construído, especificamente. | Qual é o entregável exato? |
| **C — Context** (Contexto) | Limitações do ecossistema: tokens de estilo, lógica de navegação, estados. | Onde isso vive e a que precisa obedecer? |
| **F — Format** (Formato) | Estrutura de entrega exata: Markdown, tabela, React, specs de Auto Layout. | Em que formato eu preciso receber? |

---

## Template (copie e preencha)

```text
ROLE: Atue como [especialista — ex.: Arquiteto de Design System especialista em acessibilidade WCAG].

TASK: [O que construir — ex.: "Especifique o componente de card de transação..."].

CONTEXT:
- Design tokens: [cores, espaçamento, tipografia]
- Padrões de navegação: [como o componente se conecta ao fluxo]
- Estados a cobrir: [default, hover, focus, loading, erro, vazio]

FORMAT: Entregue como [Markdown com tabela de specs | código React + Tailwind | specs de Auto Layout para Figma], incluindo [o que não pode faltar].
```

## Exemplo preenchido — Componente de card

```text
ROLE: Atue como Arquiteto de Design System especialista em acessibilidade (WCAG 2.2 AA).

TASK: Especifique o componente "Card de Transação" para o extrato de um app de finanças.

CONTEXT:
- Tokens: espaçamento base 8px; cor de sucesso #1B873F, erro #D1293D; fonte Inter.
- Navegação: ao tocar, abre o detalhe da transação (push, mesma pilha).
- Estados a cobrir: default, pressed, loading (skeleton), erro de carregamento, lista vazia.

FORMAT: Markdown com (1) tabela de anatomia, (2) tabela de estados x comportamento,
(3) checklist de acessibilidade (contraste, área de toque ≥44px, rótulo para leitor de tela).
```

---

## Dicas rápidas

- **Format é o antídoto da screen myopia:** peça sempre os estados de transição e como o componente se conecta ao fluxo, não só a tela isolada.
- Um **Role** específico ("especialista em WCAG") produz saídas melhores que um genérico ("designer").
- Para adicionar revisão automática de acessibilidade, evolua para [C-C-E-R-A](C-C-E-R-A.md).

---

📚 [← Voltar ao índice](../../README.md) · Relacionados: [C-C-E-R-A](C-C-E-R-A.md) · [CARE](CARE.md)
