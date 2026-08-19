# CRISPE — Capacity, Insight, Statement, Personality, Experiment

> Criado internamente pela **OpenAI**. Muito forte em tarefas **analíticas, técnicas e de engenharia de software**. Equilibra controle rigoroso da IA com desenvolvimento **iterativo** de soluções via testes.

| | |
|---|---|
| **Categoria** | Corporativo & Analítico (geral) |
| **Melhor para** | Problemas técnicos, análise, engenharia, exploração de múltiplas soluções |
| **Nível** | Avançado |

---

## Quando usar

Use o CRISPE quando o problema é **aberto e técnico** e você quer que a IA **proponha e compare alternativas** em vez de entregar uma resposta única. O diferencial é o **Experiment**: pedir variações para testar.

## Anatomia

| Componente | O que é | Pergunta-guia |
|---|---|---|
| **C — Capacity/Role** | O papel e a capacidade que a IA assume. | Que especialista ela encarna? |
| **I — Insight** | Contexto e background do problema. | O que ela precisa saber para raciocinar? |
| **S — Statement** | A tarefa/instrução central, objetiva. | Qual é o pedido exato? |
| **P — Personality** | O estilo/voz da resposta. | Em que tom deve responder? |
| **E — Experiment** | Pedido de múltiplas variações/abordagens para comparar. | Quais alternativas quero avaliar? |

---

## Template (copie e preencha)

```text
CAPACITY/ROLE: Aja como [especialista técnico].
INSIGHT: [Contexto do problema, restrições, stack, dados.]
STATEMENT: [A tarefa central.]
PERSONALITY: [Estilo — ex.: didático, direto, com trade-offs explícitos.]
EXPERIMENT: Ofereça [N] abordagens diferentes e compare prós/contras de cada uma.
```

## Exemplo preenchido — Arquitetura de um fluxo

```text
CAPACITY/ROLE: Aja como Arquiteto de Interação especialista em fluxos de autenticação.
INSIGHT: App móvel; usuários reclamam de fricção no login; queremos manter segurança 2FA.
STATEMENT: Proponha maneiras de reduzir o atrito do login sem enfraquecer a segurança.
PERSONALITY: Direto e técnico, sempre explicitando o trade-off segurança x conveniência.
EXPERIMENT: Apresente 3 abordagens (ex.: biometria, magic link, passkeys),
compare em fricção, segurança e esforço de implementação, e recomende uma.
```

---

## Dicas rápidas

- O **Experiment** é o coração do CRISPE — sempre peça alternativas comparadas, não uma só.
- Excelente para **decisões de design técnico** onde você quer enxergar o trade-off antes de escolher.
- Para uma decisão já definida que só precisa ser executada rápido, use [RACE](RACE.md).

---

📚 [← Voltar ao índice](../../README.md) · Relacionados: [RACE](RACE.md) · [COSTAR](COSTAR.md)
