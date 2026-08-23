# RACE — Role, Action, Context, Expectation

> Estrutura **minimalista** focada em entregas rápidas e de alta frequência. Muito adotada em **times ágeis** para automatizar documentos simples de engenharia e produto (casos de teste, PRDs) sem sobrecarregar a janela de tokens.

| | |
|---|---|
| **Categoria** | Corporativo & Analítico (geral) |
| **Melhor para** | Entregas repetitivas e padronizadas: PRDs curtos, casos de teste, tickets, resumos |
| **Nível** | Iniciante / Intermediário |

---

## Quando usar

Use o RACE quando a tarefa é **frequente, padronizada e não ambígua**, e você quer o **menor prompt possível** que ainda produz qualidade. É o equivalente "de produção" do [ICE](../01-ux-ui/ICE.md): enxuto, para rodar muitas vezes.

## Anatomia

| Componente | O que é | Pergunta-guia |
|---|---|---|
| **R — Role** (Papel) | Quem a IA encarna. | Que especialista produz isto? |
| **A — Action** (Ação) | A tarefa concreta a executar. | O que fazer, exatamente? |
| **C — Context** (Contexto) | Informação mínima necessária. | O que ela precisa saber? |
| **E — Expectation** (Expectativa) | Formato e critérios de saída. | Como eu quero receber? |

---

## Template (copie e preencha)

```text
ROLE: Aja como [papel].
ACTION: [Tarefa concreta.]
CONTEXT: [Informação essencial, sem excesso.]
EXPECTATION: [Formato + critérios — ex.: tabela, N itens, campos obrigatórios.]
```

## Exemplo preenchido — Casos de teste

```text
ROLE: Aja como QA Engineer.
ACTION: Escreva casos de teste para o formulário de recuperação de senha.
CONTEXT: Campos: e-mail; regras: e-mail válido obrigatório, limite de 3 tentativas/hora.
EXPECTATION: Tabela com colunas | ID | Cenário | Passos | Resultado esperado |,
incluindo casos felizes, de borda e de erro.
```

---

## Dicas rápidas

- Economia de tokens é uma feature: mantenha o **Context** no mínimo viável.
- Ideal para **padronizar** um tipo de entrega — salve o prompt como template do time.
- Se precisar de tom/público refinados, suba para o [COSTAR](COSTAR.md).

---

[← Voltar ao índice](../../README.md) · Relacionados: [ICE](../01-ux-ui/ICE.md) · [CRISPE](CRISPE.md)
