# Prompting Iterativo — Refino conversacional (v1 → v2 → v3)

> Constrói a resposta **em camadas**, num fluxo conversacional: gera uma base, depois aplica restrições, depois revisa. Permite edição cirúrgica de um elemento sem estragar o que já está bom (*sectional editing*).

| | |
|---|---|
| **Tipo** | Técnica de fluxo (multi-turno) |
| **Melhor para** | Refinar microcopy, textos e artefatos onde qualidade vem de camadas sucessivas |
| **Combina bem com** | [C-C-E-R-A](../frameworks/01-ux-ui/C-C-E-R-A.md) · [BAB](../frameworks/02-gerais/BAB.md) · [Autocrítica](autocritica.md) |

---

## O que é

Em vez de tentar acertar tudo num prompt gigante, você conversa em **turnos**:

- **v1 — Base:** gera as opções cruas (estrutura e quantidade).
- **v2 — Restrições:** reescreve aplicando regras estritas (o que nunca fazer, limites de tamanho).
- **v3 — Verificação:** roda uma [autocrítica](autocritica.md) e consolida a versão final.

Cada turno **preserva o que já está correto** e mexe só no que precisa (*sectional editing*), evitando que uma correção quebre outra parte.

## Quando usar

- O artefato é **sensível a nuances** (tom, acessibilidade cognitiva, voz da marca).
- Você quer **controlar a evolução** e não receber tudo de uma vez.
- Tentar embutir todas as regras num único prompt tornaria a instrução confusa.

## Como aplicar

```text
Turno 1: [gere a base — estrutura + quantidade, sem restrições ainda]
Turno 2: "Gostei da estrutura. Agora reescreva aplicando estas restrições: [regras negativas + limites]"
Turno 3: "Execute uma autocrítica contra [critérios] e entregue a versão consolidada final."
```

## Exemplo (aplicado a UX)

Microcopy de erro de pagamento construído em 3 turnos: v1 gera 3 variações em tabela → v2 aplica regras ("nunca culpar o usuário", "máx. 2 frases") → v3 faz autocrítica de acessibilidade cognitiva e consolida. Veja a receita [Microcopy de erro crítico](../receitas/ux-writing/microcopy-erro-critico.md).

## Armadilhas

- Não **reformule tudo** a cada turno — aponte só o que mudar, para preservar o que já funciona.
- Mantenha o **histórico no contexto**; se a conversa ficar longa, recapitule o estado atual.

---

[← Índice](../README.md) · Relacionadas: [Autocrítica](autocritica.md) · [Chain-of-Thought](chain-of-thought.md)
