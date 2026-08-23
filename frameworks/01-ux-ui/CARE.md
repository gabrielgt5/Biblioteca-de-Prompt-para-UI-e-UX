# CARE — Context, Ask, Rules, Examples

> Modelo tradicional do **Nielsen Norman Group**, o mais recomendado para **planejamento de pesquisa** e escrita de prompts de usabilidade.

| | |
|---|---|
| **Categoria** | UX/UI · Pesquisa & Usabilidade |
| **Origem** | Nielsen Norman Group (NN/g) |
| **Melhor para** | Planejar pesquisa de usuário, roteiros de entrevista, avaliação de usabilidade, geração de fluxos ancorados em contexto real |
| **Nível** | Intermediário |

---

## Quando usar

Use o CARE quando a qualidade da resposta depende de **quem é o usuário** e de **regras de negócio/acessibilidade** que a IA não pode ignorar. É o framework mais forte para tarefas de descoberta e pesquisa, porque obriga você a declarar o cenário antes do pedido.

## Anatomia

| Componente | O que é | Pergunta-guia |
|---|---|---|
| **C — Context** (Contexto) | Cenário, sua função, o produto e o usuário final. | Quem sou eu, o que é o produto e para quem? |
| **A — Ask** (Pedido) | A ação ou pergunta clara e objetiva para o modelo. | O que eu quero que seja gerado, em uma frase? |
| **R — Rules** (Regras) | Diretrizes, limitações e regras estritas de negócio, acessibilidade ou tom de voz. | O que é obrigatório e o que é proibido? |
| **E — Examples** (Exemplos) | Demonstrações reais de uma saída ideal, para ancorar o padrão visual ou de escrita. | Como se parece uma boa resposta? |

---

## Template (copie e preencha)

```text
# CONTEXT
Sou um(a) [função/senioridade] trabalhando em [produto/feature] para [público-alvo].
O objetivo do projeto é [meta]. Restrições do ambiente: [plataforma, mercado, momento].

# ASK
[Ação clara e objetiva. Ex.: "Gere um roteiro de 8 perguntas para entrevista..."]

# RULES
- [Regra de negócio]
- [Regra de acessibilidade — ex.: WCAG 2.2 AA]
- [Tom de voz / limitações — ex.: sem jargão, no máximo X itens]

# EXAMPLES
Exemplo de saída ideal:
[Cole um trecho real do padrão que você espera — pergunta modelo, microcopy, etc.]
```

## Exemplo preenchido — Pesquisa de onboarding

```text
# CONTEXT
Sou UX Designer sênior no onboarding de um app de finanças B2B para millennials
que abrem a primeira conta PJ. O objetivo é reduzir a evasão nas 3 primeiras telas.

# ASK
Gere um roteiro de entrevista de descoberta com 8 perguntas para entender por que
usuários abandonam o cadastro.

# RULES
- Perguntas abertas, sem induzir resposta (não usar "você não acha que...").
- Linguagem simples, evitar termos bancários técnicos.
- Incluir 2 perguntas sobre confiança/segurança percebida.

# EXAMPLES
Pergunta modelo (tom desejado):
"Me conta como foi a última vez que você desistiu de um cadastro pela metade —
o que estava acontecendo naquele momento?"
```

---

## Dicas rápidas

- **Context primeiro, sempre.** Sem contexto, o modelo assume um usuário genérico e a saída perde precisão.
- Em **Examples**, um exemplo do padrão desejado vale mais que três parágrafos de instrução.
- Combine com [C-C-E-R-A](C-C-E-R-A.md) quando quiser adicionar uma camada de autocrítica técnica.

---

[← Voltar ao índice](../../README.md) · Relacionados: [ICE](ICE.md) · [RTCF](RTCF.md)
