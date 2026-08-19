---
titulo: Arquitetura de Fluxo de Onboarding
tarefa: Onboarding
frameworks: [CARE]
tecnicas: [Chain-of-Thought, Decomposição / Step Zero]
nivel: Avançado
---

# Arquitetura de Fluxo de Onboarding

> Projeta a **lógica da jornada completa** de um onboarding antes de detalhar telas — evitando o vício de gerar "telas soltas" (*screen myopia*).

| | |
|---|---|
| **Tarefa** | Onboarding |
| **Framework** | [CARE](../../frameworks/01-ux-ui/CARE.md) |
| **Técnica** | [Chain-of-Thought](../../tecnicas/chain-of-thought.md) + [Decomposição / Step Zero](../../tecnicas/decomposicao-step-zero.md) |
| **Nível** | Avançado |

---

## 🎯 Objetivo

Evitar o vício de gerar telas isoladas sem conexão de fluxo. O prompt usa o **CARE** (Nielsen Norman Group) e força o modelo a **pensar passo a passo** na jornada completa do usuário **antes** de detalhar elementos visuais (aplicando a lógica do "Step Zero").

## 🧩 Framework + Técnica

O **CARE** ancora a tarefa em contexto real (produto, usuário, meta de negócio). O **Chain-of-Thought** obriga a resolver a lógica da jornada antes do layout — a combinação garante que cada tela tenha um papel dentro do todo, e não seja um retângulo bonito e desconexo.

## 📋 O Prompt

```text
# CONTEXTO (CARE - Context)
Atue como um Designer de Interação Sênior focado em usabilidade móvel. Estou redesenhando o fluxo de onboarding para um aplicativo financeiro de investimentos voltado para jovens adultos (geração Z) que nunca investiram antes. O objetivo do negócio é reduzir o abandono na etapa de verificação de identidade (KYC).

# PEDIDO (CARE - Ask)
Desenvolva a lógica e a arquitetura de telas para um fluxo de onboarding de 3 a 4 telas, cobrindo desde as boas-vindas até o primeiro depósito simbólico.

Antes de detalhar as telas, você deve realizar um processo de Chain-of-Thought. Siga estes passos de forma estrita:
1. Analise as 3 principais fricções cognitivas que um usuário iniciante enfrenta ao abrir um app de finanças.
2. Mapeie a jornada ideal de transição lógica entre cada uma das 4 telas do fluxo.
3. Para cada tela, deduza quais informações mínimas são estritamente necessárias para evitar sobrecarga de informação.
4. Só depois de concluir as análises acima, estruture o layout e os componentes recomendados de cada tela.

# REGRAS (CARE - Rules)
- NUNCA sugira solicitar dados pessoais invasivos (como CPF ou endereço) na primeira tela de boas-vindas.
- Evite adjetivos abstratos como "moderno" ou "elegante". Seja específico quanto a componentes (ex: stepper indicador de progresso, botão de CTA principal, campos de entrada de formulário).
- Respeite as boas práticas de acessibilidade de toque móvel (touch target mínimo de 48x48dp).

# EXEMPLO (CARE - Example)
Apresente a saída final no seguinte formato estruturado:
- **Fase de Análise Cognitiva:** [Insira sua análise passo a passo aqui]
- **Arquitetura do Fluxo:** [Tela 1 -> Tela 2 -> Tela 3 -> Tela 4]
- **Especificação por Tela:**
  * **Objetivo da Tela:**
  * **Elementos de UI Requeridos:** (botões, inputs, imagens)
  * **Estratégia de Redução de Fricção:** (por que essa tela é estruturada assim?)
```

## ▶️ Como usar

1. Troque o **contexto** (produto, público, meta de negócio) pelo seu caso real.
2. Ajuste o **número de telas** conforme o fluxo (3–4 costuma ser o ideal para onboarding).
3. Revise as **regras** — as regras negativas ("NUNCA…") são o que mais direciona a qualidade.
4. Mantenha o **formato de saída** para receber a análise separada da especificação.

## 💡 Por que funciona

Divide uma tarefa de alta complexidade em partes ordenadas (**decomposição**), reduz drasticamente o risco de layouts caóticos, garante conformidade com uma meta real de negócio (**conversão no KYC**) e respeita acessibilidade e usabilidade **desde o primeiro turno**.

## 🔁 Variações

- **Mais rigor técnico:** troque o CARE por [C-C-E-R-A](../../frameworks/01-ux-ui/C-C-E-R-A.md) para adicionar um passo de [autocrítica](../../tecnicas/autocritica.md) de acessibilidade ao final.
- **Handoff para dev:** peça o formato de saída em specs de [RTCF](../../frameworks/01-ux-ui/RTCF.md) (código/Auto Layout).
- **Outros fluxos:** funciona para checkout, cadastro, upgrade de plano — troque a meta de negócio.

## 🔗 Relacionados

- Framework: [CARE](../../frameworks/01-ux-ui/CARE.md)
- Técnicas: [Chain-of-Thought](../../tecnicas/chain-of-thought.md) · [Decomposição / Step Zero](../../tecnicas/decomposicao-step-zero.md)

---

📚 [← Índice](../../README.md)
