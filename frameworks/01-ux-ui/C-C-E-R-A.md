# C-C-E-R-A — Clareza, Contexto, Especificidade, Referência Visual e Autocrítica

> Framework proposto na literatura científica em português sobre **modelagem de contexto em UI/UX**. Atua como uma **síntese integradora** de outros modelos, com um diferencial: o ciclo de **autocrítica** antes da entrega.

| | |
|---|---|
| **Categoria** | UX/UI · Alta fidelidade & Qualidade técnica |
| **Melhor para** | Telas de alta fidelidade para desenvolvimento, quando acessibilidade e robustez lógica são críticas |
| **Nível** | Avançado |

---

## Quando usar

Use o C-C-E-R-A quando você **não pode revisar manualmente** cada detalhe e precisa que o próprio modelo faça a auditoria. A autocrítica neutraliza os três erros mais comuns de geração de UI: **contêineres vazios**, **falta de hierarquia** e **falhas de lógica** entre estados/telas.

## Anatomia

| Componente | O que é | Pergunta-guia |
|---|---|---|
| **C — Clareza** | Instrução direta, sem ambiguidade. | O pedido pode ser interpretado de um jeito só? |
| **C — Contexto** | Produto, usuário, ecossistema e restrições. | Onde isso vive e para quem? |
| **E — Especificidade** | Detalhe técnico: tokens, estados, dados de exemplo. | Dei dados concretos ou deixei o modelo adivinhar? |
| **R — Referência Visual** | Padrão visual/estrutural a seguir (exemplo, sistema, print). | Qual referência ancora o resultado? |
| **A — Autocrítica** | Ciclo de revisão interna antes da resposta final. | O modelo testou a própria proposta? |

### O componente que faz a diferença: Autocrítica (Evaluation)

Antes de entregar, o modelo deve:

1. **Testar contra heurísticas clássicas** de usabilidade (ex.: Nielsen).
2. **Verificar acessibilidade** — contraste, foco, rótulos para leitores de tela.
3. **Prever estados de erro e transição** entre telas (loading, vazio, falha, sucesso).
4. **Reportar o que corrigiu** antes de mostrar a versão final.

---

## Template (copie e preencha)

```text
CLAREZA (instrução): [Um pedido inequívoco, uma frase.]

CONTEXTO: [Produto, usuário, plataforma, objetivo de negócio.]

ESPECIFICIDADE:
- Tokens/dados: [cores, espaçamento, conteúdo de exemplo real]
- Estados obrigatórios: [default, loading, vazio, erro, sucesso]

REFERÊNCIA VISUAL: [Padrão a seguir — sistema de design, exemplo, print, descrição.]

AUTOCRÍTICA (obrigatória antes de responder):
Antes de me entregar a versão final, revise sua própria proposta:
1. Teste contra as heurísticas de Nielsen e liste violações encontradas.
2. Verifique acessibilidade (contraste AA, área de toque, rótulos p/ leitor de tela).
3. Garanta que todos os estados (vazio, erro, loading) foram tratados.
4. Corrija os problemas e me mostre um resumo do que ajustou + a versão final.
```

## Exemplo preenchido — Tela de listagem

```text
CLAREZA: Projete a tela de "Minhas faturas" de um app de cartão de crédito.

CONTEXTO: App B2C, usuários 30–55 anos, muitos com baixa familiaridade digital.
Meta: reduzir chamados de "não encontrei minha fatura".

ESPECIFICIDADE:
- Tokens: base 8px, primária #2D5BFF, fonte Inter.
- Dados de exemplo: 3 faturas (paga, em aberto, vencida).
- Estados obrigatórios: lista com itens, lista vazia, erro de carregamento, loading.

REFERÊNCIA VISUAL: padrão de lista com cabeçalho fixo e chips de status coloridos.

AUTOCRÍTICA (antes da resposta final):
1. Cheque contra as heurísticas de Nielsen (visibilidade de status, prevenção de erro).
2. Confirme contraste AA dos chips de status e rótulos para leitor de tela.
3. Trate os 4 estados; não deixe contêiner vazio sem mensagem orientativa.
4. Resuma correções e entregue a versão final.
```

---

## Dicas rápidas

- É o mais completo dos frameworks de UX/UI — use quando o custo de um erro de UI é alto.
- A **Autocrítica** só funciona se você **exigir o relatório** das correções; sem isso, o modelo pula a etapa.
- É a evolução natural do [RTCF](RTCF.md) quando você precisa de garantia de acessibilidade.

---

[← Voltar ao índice](../../README.md) · Relacionados: [RTCF](RTCF.md) · [CARE](CARE.md)
