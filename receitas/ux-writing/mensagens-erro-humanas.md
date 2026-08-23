---
titulo: Mensagens de Erro Humanas (3 Dimensões)
tarefa: UX Writing
frameworks: [RTCF]
tecnicas: [Few-Shot, Autocrítica]
nivel: Intermediário
---

# Mensagens de Erro Humanas — as 3 Dimensões

> Gera mensagens de erro **acessíveis, sem culpa e acionáveis** num único prompt, aplicando as três dimensões (Visibilidade, Comunicação, Eficiência) e a fórmula de redação `[o que falhou] + [o porquê] + [a ação]`.

| | |
|---|---|
| **Tarefa** | UX Writing |
| **Framework** | [RTCF](../../frameworks/01-ux-ui/RTCF.md) |
| **Técnica** | [Few-Shot](../../tecnicas/few-shot.md) + [Autocrítica](../../tecnicas/autocritica.md) |
| **Nível** | Intermediário |

---

## Objetivo

Produzir mensagens de erro que respeitam a dignidade, a atenção e o tempo do usuário. O prompt embute um *rulebook* completo (as 3 dimensões), a fórmula de 3 partes e exemplos antes→depois, mais um passo de autocrítica que verifica acessibilidade e "efeito copiloto" (mensagem polida, porém vazia de ação).

## Framework + Técnica

O **RTCF** dá o esqueleto (papel, tarefa, contexto do erro e o **formato** — a fórmula obrigatória). O **Few-Shot** ancora a qualidade com transformações antes→depois. A **Autocrítica** final garante que nenhuma regra crítica (culpa, jargão, contraste, ação ausente) escapou.

## As 3 dimensões (referência rápida)

| Dimensão | Regra central |
|---|---|
| **Visibilidade** | Erro adjacente ao campo (não em modal/topo) · nunca só cor: texto + ícone + borda · contraste ≥ 4.5:1 · validar no *blur*/envio, nunca durante a digitação |
| **Comunicação** | Linguagem simples (6º–8º ano) · sem códigos técnicos · sem culpa ("Não conseguimos…") · 12–18 palavras |
| **Eficiência** | Nunca apagar o que foi digitado · sempre dar a solução pragmática (formato esperado / atalho), não só o diagnóstico |

**Fórmula de redação:** `[O que falhou]` + `[O porquê / contexto]` + `[A ação resolutiva]`

## O Prompt

```text
#### ROLE
Você é um(a) UX Writer sênior especialista em mensagens de erro acessíveis e humanas.
Domina WCAG 2.2 AA, linguagem simples (nível 6º–8º ano) e escrita sem culpa (atribuição sistêmica).

#### TASK
Escreva a mensagem de erro para o cenário abaixo, seguindo a FÓRMULA obrigatória e as REGRAS das 3 dimensões.

#### CONTEXT (o cenário)
- Produto: [ex.: e-commerce / app bancário]
- Falha (descreva objetivamente o estado do sistema): [ex.: upload de arquivo excedeu o limite]
- Onde a mensagem aparece: [campo do formulário / etapa / tela]
- Público e estado emocional provável: [ex.: usuário apressado finalizando compra]

#### FORMAT — Fórmula obrigatória
Toda mensagem segue: [O que falhou] + [O porquê/contexto] + [A ação resolutiva].
Entregue:
- **Título:** ≤ 8 palavras
- **Corpo:** 12–18 palavras, 1–2 frases curtas
- **CTA:** rótulo com verbo de ação que resolve
- **Nota de implementação:** onde/como exibir (visibilidade) e os 3 sinalizadores visuais

#### REGRAS (as 3 dimensões — inegociáveis)
Visibilidade:
- Exibir adjacente à origem do erro (ex.: abaixo do campo), nunca em modal genérico ou alerta no topo.
- Nunca depender só de cor: use 3 sinalizadores coordenados (texto + ícone de alerta + borda/contraste).
- Contraste do texto ≥ 4.5:1 (WCAG AA).
- Não validar durante a digitação; disparar só ao sair do campo (blur) ou no envio.
Comunicação:
- Linguagem simples (6º–8º ano). Proibido código técnico ("Erro 4002", "invalid JSON"); se essencial p/ suporte, ocultar em "ver detalhes".
- Isenção de culpa: o sistema assume a responsabilidade. Proibidas as palavras: "inválido", "ilegal", "você falhou", "incorreto".
- Brevidade: 12–18 palavras; prefira frases de até 8 palavras.
Eficiência:
- Nunca apague o que o usuário digitou; permita editar o original.
- Dê a ação pragmática: indique o formato esperado (ex.: DD/MM/AAAA) ou um atalho de resolução — não só o diagnóstico.

#### EXEMPLOS (antes → depois)
1. Senha
   Antes: "Senha inválida. O preenchimento requer parâmetros mínimos de segurança criptográfica."
   Depois: "Escolha uma senha com pelo menos 8 caracteres e uma letra maiúscula."
2. Cartão recusado
   Antes: "Transação recusada. Falha na autenticação do cartão. Contate o emissor."
   Depois: "Não conseguimos concluir a cobrança. Confira se o número do cartão e o CVV estão corretos."
3. Estado vazio (404/sem dados)
   Antes: "Erro 404: Nenhum dado localizado na base atual."
   Depois: "Seus relatórios aparecerão aqui. Clique abaixo para gerar seu primeiro painel."

#### AUTOCRÍTICA (execute antes de entregar)
Revise sua proposta contra os critérios e corrija o que falhar:
1. Cumpre a fórmula (o que falhou + porquê + ação)?
2. Tem 12–18 palavras, sem culpa e sem jargão técnico?
3. Visibilidade ok? (posição adjacente, 3 sinalizadores, contraste ≥ 4.5:1)
4. Existe uma ação concreta que responde "o que eu faço agora?" — não só diagnóstico?
5. Zero humor em contexto sensível (pagamento, conta bloqueada).
Entregue: (a) a versão final + (b) uma linha resumindo o que ajustou na autocrítica.
```

## Como usar

1. Preencha só o bloco **CONTEXT** com o seu cenário de erro real.
2. Mantenha as **REGRAS** e os **EXEMPLOS** — são eles que garantem a qualidade e o tom.
3. Se sua marca tem voz própria, acrescente 1 exemplo antes→depois no estilo dela ([Few-Shot](../../tecnicas/few-shot.md)).
4. Leia a linha de **autocrítica** que o modelo devolve: é onde você audita se ele cumpriu as regras.

## Por que funciona

Transforma teoria de UX em **restrições verificáveis**: a fórmula garante ação (não só diagnóstico), as regras negativas eliminam culpa e jargão, os exemplos antes→depois fixam o padrão, e a autocrítica combate o **"efeito copiloto"** — mensagens gramaticalmente perfeitas, porém vazias da única linha que importa: *"o que eu faço agora?"*.

## Exemplos de transformação

| Contexto | Antes (tecnocêntrico) | Depois (humano) |
|---|---|---|
| Senha | "Senha inválida. Parâmetros mínimos de segurança não cumpridos." | "Escolha uma senha com pelo menos 8 caracteres e uma letra maiúscula." |
| Cartão | "Transação recusada. Falha na autenticação. Contate o emissor." | "Não conseguimos concluir a cobrança. Confira o número do cartão e o CVV." |
| Vazio/404 | "Erro 404: Nenhum dado localizado." | "Seus relatórios aparecerão aqui. Gere seu primeiro painel abaixo." |

## Armadilhas críticas

- **Humor na hora errada:** quem tenta pagar ou recuperar uma conta bloqueada não quer piada ("gremlins no servidor"). Regra do Mailchimp: *na dúvida, mantenha a seriedade*.
- **Efeito copiloto de IA:** a IA produz texto polido, mas costuma esquecer a ação resolutiva. Exija regras rígidas (este prompt) e faça sempre **curadoria humana final**.

## Variações

- **Sistema inteiro de erros:** peça uma tabela cobrindo vários cenários de uma vez, mantendo fórmula e regras.
- **Refino em camadas:** combine com o fluxo de 3 turnos da receita [Microcopy de erro crítico](microcopy-erro-critico.md).
- **Empty states:** o mesmo rulebook serve para estados vazios; combine com [BAB](../../frameworks/02-gerais/BAB.md).

## Relacionados

- Framework: [RTCF](../../frameworks/01-ux-ui/RTCF.md)
- Técnicas: [Few-Shot](../../tecnicas/few-shot.md) · [Autocrítica](../../tecnicas/autocritica.md)
- Receita irmã: [Microcopy de erro crítico](microcopy-erro-critico.md)

---

[← Índice](../../README.md)
