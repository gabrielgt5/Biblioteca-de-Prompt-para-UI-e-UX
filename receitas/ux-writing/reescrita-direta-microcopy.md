---
titulo: Reescrita Direta de Microcopy (Plug-and-Play)
tarefa: UX Writing
frameworks: [RTCF]
tecnicas: [Zero-Shot]
nivel: Intermediário
---

# Reescrita Direta de Microcopy (Plug-and-Play)

> Substitui, de forma **cirúrgica**, os textos que já existem numa tela desenhada (mockup ou produção) por versões de alta performance — **mantendo a estrutura do layout intacta**. A saída vem numa tabela Antes→Depois, pronta para colar no Figma ou no código.

| | |
|---|---|
| **Tarefa** | UX Writing |
| **Framework** | [RTCF](../../frameworks/01-ux-ui/RTCF.md) |
| **Técnica** | [Zero-Shot](../../tecnicas/zero-shot.md) |
| **Nível** | Intermediário |

---

## Objetivo

Otimizar o microcopy de uma tela **já existente** sem redesenhar nada. Você fornece os textos atuais e recebe versões claras, humanas e resolutivas com a mesma extensão aproximada — de modo que nada estoure o layout. É o modo "mapeamento direto": entra texto atual, sai texto otimizado.

## Framework + Técnica

O **RTCF** dá a estrutura completa (papel, contexto do produto/persona, tarefa com regras e formato de saída). A técnica é **Zero-Shot**: instrução direta com restrições rígidas, sem exemplos — o próprio texto da tela é a entrada a transformar. A restrição de compatibilidade de layout é o que diferencia esta receita das outras de UX Writing.

## O Prompt

Preencha as variáveis `{...}` e a seção **Mapeamento de Entrada** com os textos reais da sua tela antes de colar na IA.

```text
# PAPEL (ROLE)
Atue como um UX Writer Sênior e Especialista em Engenharia de Conteúdo de Interfaces Digitais. Sua especialidade é otimizar textos de interface (microcopy) existentes para que se tornem claros, humanos, resolutivos e de baixo custo cognitivo, sem alterar a estrutura de componentes do layout original.

# CONTEXTO (CONTEXT)
* PRODUTO/SISTEMA: {Descreva o produto, ex: Aplicativo de entrega de comida para bairros locais}
* TELA ATUAL: {Descreva a tela, ex: Etapa de confirmação de endereço de entrega}
* PERSONA DO USUÁRIO: {Descreva quem usa, ex: Usuário casual, com pressa, querendo pedir o almoço rapidamente}
* ESTADO EMOCIONAL: {Ex: Ansioso, com fome, impaciente}

# TAREFA (TASK) - DIRETRIZES DE REESCRITA DIRETA
Você receberá abaixo os textos exatos que já estão na minha tela atual. Sua tarefa é reescrever cada um deles de forma cirúrgica. Siga rigorosamente estes parâmetros científicos de UX Writing:

1. COMPATIBILIDADE DE LAYOUT (RESTRICÃO FÍSICA):
   - Mantenha a mesma quantidade e estrutura de caracteres aproximada (se o texto original for curto, a reescrita deve ser curta para não estourar o design da tela).
   - Não adicione componentes novos que não existam na lista.

2. LINGUAGEM SIMPLES E VOZ ATIVA:
   - Elimine jargões e simplifique o nível de leitura para o 6º ao 8º ano escolar.
   - Use voz ativa em pelo menos 85% do conteúdo para manter as frases dinâmicas e diretas.

3. ISENÇÃO DE CULPA (ATRIBUIÇÃO SISTÊMICA):
   - Elimine palavras acusatórias ou punitivas (como "inválido", "erro seu", "falhou", "incorreto").
   - Transfira a carga do erro de forma amigável para o sistema ou mostre uma solução direta.

4. DIRECIONAMENTO RESOLUTIVO (FRONT-LOADING):
   - Comece as frases e comandos sempre pelos verbos de ação mais significativos (ex: em vez de "Para atualizar clique aqui", use "Atualize seu endereço para continuar").
   - Nunca deixe o usuário em um beco sem saída; forneça saídas claras.

5. COMBATE AO "AI SLOP":
   - Proibido usar termos artificiais como: "explore", "revolucione", "potencialize", "desvende", "simplifique", "de forma fácil".

---

# TEXTOS ATUAIS DA MINHA TELA (MAPEAMENTO DE ENTRADA)
Substitua os textos de exemplo abaixo pelos textos reais que estão na sua tela hoje:

* [Título da Tela]: "Localização não localizada pelo satélite do sistema."
* [Helper Text / Texto de Apoio]: "Para que o fluxo possa prosseguir de maneira adequada, torna-se obrigatória a digitação de um endereço válido no campo inferior."
* [Placeholder do Input]: "Digite as informações de endereço aqui..."
* [CTA / Botão Principal]: "Efetuar a validação do endereço cadastrado"
* [Link / Saída de Escape]: "Voltar"

---

# FORMATO DE SAÍDA (FORMAT)
Gere uma tabela de mapeamento direto (Antes vs. Depois) que eu possa copiar e colar direto na minha ferramenta de design (Figma) ou código. Não adicione introduções ou conclusões de IA. Comece diretamente na tabela:

| Componente da Tela | Cópia Atual (Antes) | Cópia Otimizada (Depois) | Por que essa mudança funciona? (Justificativa UX) |
| :--- | :--- | :--- | :--- |
| **[Título da Tela]** | "Localização não localizada pelo satélite do sistema." | {Sua proposta curta e sem jargões} | {Foco na clareza do status} |
| **[Helper Text]** | "Para que o fluxo..." | {Sua proposta com voz ativa e isenção de culpa} | {Foco no custo cognitivo e front-loading} |
| **[Placeholder]** | "Digite as informações..." | {Sua proposta simples} | {Melhoria de usabilidade} |
| **[CTA / Botão]** | "Efetuar a validação..." | {Sua proposta resolutiva e curta} | {Foco na ação direta} |
| **[Link / Escape]** | "Voltar" | {Sua proposta de escape} | {Foco em manter o controle do usuário} |
```

## Como usar

1. Preencha as variáveis `{...}` do bloco **CONTEXTO** com o seu produto, tela e persona.
2. No **Mapeamento de Entrada**, cole os textos reais da tela (um por componente).
3. Ajuste a lista de componentes conforme a sua tela: remova os que não existem, acrescente os que faltarem — mantendo o mesmo padrão de linha.
4. Cole na IA e receba a tabela Antes→Depois pronta para o Figma/código.

## Por que funciona

A restrição de **compatibilidade de layout** impede que o texto otimizado quebre o design — o problema mais comum ao reescrever copy de telas prontas. O **front-loading** (verbo primeiro) e a **isenção de culpa** aumentam clareza e reduzem fricção, enquanto a lista anti-"AI slop" corta o vocabulário artificial que denuncia texto gerado por IA. O formato de **tabela direta, sem introduções**, entrega algo colável na hora.

## Variações

- **Tela inteira de uma vez:** liste todos os componentes de uma tela complexa (formulário longo, checkout) no mapeamento de entrada.
- **Com fórmula de erro:** para estados de erro, combine com o rulebook da receita [Mensagens de erro humanas](mensagens-erro-humanas.md).
- **Refino em camadas:** se quiser evoluir a saída, encadeie com o fluxo de 3 turnos de [Microcopy de erro crítico](microcopy-erro-critico.md).

## Relacionados

- Framework: [RTCF](../../frameworks/01-ux-ui/RTCF.md)
- Técnica: [Zero-Shot](../../tecnicas/zero-shot.md)
- Receitas irmãs: [Mensagens de erro humanas](mensagens-erro-humanas.md) · [Microcopy de erro crítico](microcopy-erro-critico.md)

---

[← Índice](../../README.md)
