---
titulo: Microcopy de Erro Crítico
tarefa: UX Writing
frameworks: [C-C-E-R-A]
tecnicas: [Prompting Iterativo, Autocrítica]
nivel: Intermediário
---

# Microcopy de Erro Crítico

> Refina de forma **cirúrgica** as mensagens de um estado de erro num fluxo conversacional de 3 turnos (v1 → v2 → v3), sem estragar o que já está correto.

| | |
|---|---|
| **Tarefa** | UX Writing |
| **Framework** | [C-C-E-R-A](../../frameworks/01-ux-ui/C-C-E-R-A.md) |
| **Técnica** | [Prompting Iterativo](../../tecnicas/prompting-iterativo.md) + [Autocrítica](../../tecnicas/autocritica.md) |
| **Nível** | Intermediário |

---

## Objetivo

Refinar um elemento específico da interface (técnica de *sectional editing*) sem alterar o que já está correto. Constrói a qualidade **em camadas**: base → restrições estritas → verificação de acessibilidade.

## Framework + Técnica

O **prompting iterativo** separa o trabalho em 3 turnos, cada um preservando o acerto do anterior. O turno final aplica a **autocrítica** do [C-C-E-R-A](../../frameworks/01-ux-ui/C-C-E-R-A.md), garantindo acessibilidade cognitiva para usuários sob estresse.

## O Prompt (fluxo de 3 turnos)

### Turno 1 — Gerando a base (v1)

```text
Atue como um UX Writer experiente. Analise o seguinte cenário de erro: O usuário está tentando finalizar uma compra internacional em nosso e-commerce, mas o cartão dele foi recusado pelo banco emissor por falta de limite disponível.

Crie uma tabela Markdown contendo 3 variações de mensagens de erro amigáveis para essa situação. A tabela deve conter as colunas:
| Tom | Título da Mensagem | Texto de Apoio (Helper Text) | Texto do Botão de Ação (CTA) |
```

### Turno 2 — Restrições estritas de redação (v2)

*(Insira após a resposta inicial da IA)*

```text
Gostei da estrutura, mas precisamos refinar sob regras corporativas estritas (v2). Reescreva as 3 opções aplicando as seguintes restrições:
- NUNCA use jargões técnicos ou códigos de erro incompreensíveis (como "Erro de Processamento de Crédito").
- NUNCA culpe o usuário (evite termos como "Você digitou dados incorretos" ou "Seu saldo é insuficiente"). Descreva o estado do sistema objetivamente.
- Forneça sempre um passo de recuperação acionável no botão de CTA (ex: incentivar a troca de método de pagamento).
- Cada mensagem de erro deve ter no máximo 2 frases.
```

### Turno 3 — Autocrítica e consolidação (v3)

*(Insira após a resposta refinada da IA)*

```text
Agora, execute um passo de autocrítica técnica (v3). Analise as mensagens propostas contra os seguintes critérios:
1. Elas respeitam as diretrizes de acessibilidade cognitiva? (Pessoas sob estresse no fluxo de compra conseguirão entender facilmente o que fazer?)
2. Há alguma palavra que possa causar ansiedade ou frustração desnecessária?

Apresente uma versão consolidada final baseada na sua autocrítica.
```

## Como usar

1. **Turno 1:** troque o cenário de erro pelo seu caso; receba a base em tabela.
2. **Turno 2:** ajuste as regras negativas conforme a voz da sua marca e limites de tamanho.
3. **Turno 3:** rode a autocrítica; use os critérios de acessibilidade cognitiva do seu contexto.
4. Não reformule tudo a cada turno — aponte só o que mudar, preservando o que já ficou bom.

## Por que funciona

O refino incremental constrói qualidade em camadas, e o *sectional editing* evita que uma correção quebre outra parte. As **regras negativas** ("nunca culpar o usuário") e a **autocrítica final** garantem microcopy honesto e acessível para quem está sob estresse.

## Variações

- **Empty states / notificações:** mesmo fluxo, troque o cenário; combine com [BAB](../../frameworks/02-gerais/BAB.md).
- **Mais variações:** peça 5 opções no turno 1 para ter mais material a filtrar.
- **Tom de voz:** adicione um turno 2b fixando a voz da marca com exemplos ([Few-Shot](../../tecnicas/few-shot.md)).

## Relacionados

- Framework: [C-C-E-R-A](../../frameworks/01-ux-ui/C-C-E-R-A.md)
- Técnicas: [Prompting Iterativo](../../tecnicas/prompting-iterativo.md) · [Autocrítica](../../tecnicas/autocritica.md)

---

[← Índice](../../README.md)
