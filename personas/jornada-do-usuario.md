# Mapa de Jornada do Usuário

> Gera um **Mapa de Jornada do Usuário** detalhado, em tabela Markdown, ancorado em briefing + persona + dados de pesquisa. As mesmas regras anti-clichê das personas se aplicam (pilha de ferramentas coesa, metas mensuráveis, dores operacionais, espaço negativo de rejeição, carga cognitiva).

## Objetivo

Transformar briefing, persona e pesquisa em uma **infraestrutura real de design de interface** — não uma jornada genérica. O prompt força análise qualitativa em prosa (sem bullets nas células), curva emocional justificada e oportunidades de design ligadas a gargalos concretos. Escolhe-se entre uma jornada **SaaS tradicional** (Opção A) ou **era da IA / busca generativa** (Opção B).

## O Prompt

Preencha o `BRIEFING`, a `PERSONA` e os `DADOS DE PESQUISA` ao final, e escolha **uma** das duas opções de fases.

```text
Você atuará como um Pesquisador Sênior de Experiência do Usuário (UX Researcher) e Designer de Serviços com ampla vivência em arquitetura de informação e modelagem de produtos digitais complexos. Sua tarefa consiste em analisar minuciosamente o BRIEFING DE PROJETO, a PERSONA e os DADOS DE PESQUISA apresentados e gerar um Mapa de Jornada do Usuário altamente detalhado e estruturado.

Para evitar os clichês usuais de simplificação comportamental e garantir que a jornada funcione como uma infraestrutura real de design de interface, as seguintes REGRAS DE CONTROLE devem ser aplicadas de forma estrita durante toda a geração:

REGRAS DE CONTROLE E SISTEMA:
1. COESÃO DA PILHA DE FERRAMENTAS: Descreva o ecossistema real de softwares que a persona opera em sua rotina. Evite incluir ferramentas que concorram diretamente para uma mesma finalidade (como uso simultâneo de HubSpot e Salesforce) sem uma justificativa explícita de fluxo técnico de trabalho.
2. METAS MENSURÁVEIS E TEMPORAIS: Proíba resoluções e objetivos vagos que se apliquem a qualquer ser humano (como "deseja economizar tempo" ou "busca eficiência"). Todas as metas descritas devem ser quantificáveis e realizáveis em prazos determinados (ex: "reduzir em 45% o tempo de digitação manual de faturas mensais até o encerramento do trimestre fiscal atual").
3. PONTOS DE FRUSTRAÇÃO CONCRETOS E OPERACIONAIS: Detalhe os gargalos operacionais específicos em sistemas reais, descrevendo exatamente em qual etapa do fluxo ou do software legado ocorrem as falhas de usabilidade. Não utilize sofrimentos subjetivos inventados apenas para justificar as soluções sugeridas no briefing.
4. ESPAÇO NEGATIVO DE REJEIÇÃO: Toda jornada deve evidenciar o que a persona rejeita. Descreva com exatidão uma funcionalidade ou elemento de design listado no briefing que a persona especificamente NÃO queira em sua rotina, explicando as razões pelas quais esse recurso geraria complexidade desnecessária para o perfil dela.
5. PARÂMETROS DE CARGA COGNITIVA E INTERAÇÃO: Especifique categoricamente:
   - Tolerância à Carga Cognitiva: [Alta / Média / Baixa - Justifique o nível detalhadamente]
   - Densidade de Dados Preferencial na Tela: [Alta Densidade de Dados (tabelas densas, filtros persistentes) / Exibição Espaçosa e Linear (fluxos guiados, progressive disclosure)]
   - Perfil de Navegação Física: [Ex: Dependente de atalhos de teclado / Operação exclusiva em ambiente mobile com foco no toque / Uso de ferramentas assistivas]

ESTRUTURA DA TABELA DO MAPA DE JORNADA:
Você deve apresentar o Mapa de Jornada do Usuário no formato exclusivo de uma Tabela Markdown. Não utilize listas de tópicos (bullet points) nas células para manter o rigor analítico; preencha cada campo com análises qualitativas ricas em prosa contínua e transições de ambiente (online para offline).

A tabela deve seguir rigorosamente a seguinte estrutura de cabeçalho:
| Fase da Jornada | Atividade e JTBD (O que tenta realizar) | Ações e Canais (Como realiza e onde) | Pensamentos e Mentalidade (Dúvidas/Expectativas) | Curva Emocional (Alegria/Frustração - Justificar) | Gargalos e Dores (Onde o processo falha) | Oportunidades de Design (Como o produto pode resolver) |

[ESCOLHA APENAS UM DOS DOIS CONJUNTOS DE FASES ABAIXO CONFORME O SEU CONTEXTO]:

--- OPÇÃO A: JORNADA TRADICIONAL/SaaS ---
Utilize as seguintes fases de ciclo de vida para estruturar as linhas da tabela:
- **1. Descoberta & Alinhamento**
- **2. Configuração Inicial**
- **3. Primeiro Uso Principal (Aha! Moment)**
- **4. Uso Rotineiro & Integração**
- **5. Suporte & Resolução de Problemas**

--- OPÇÃO B: JORNADA NA ERA DA IA / BUSCA GERATIVA ---
Utilize as seguintes fases de comportamento adaptativo para estruturar as linhas da tabela:
- **1. Forrageamento de Palavras-Chave** (O usuário realiza buscas preliminares em motores tradicionais para entender e capturar a terminologia adequada antes de formular sua pergunta na IA)
- **2. Formulação Detalhada do Prompt** (Redação de comandos longos, de 6 a 9 palavras, que combinam vários objetivos de pesquisa e intenções em uma única interação)
- **3. Fase do Canal Invisível** (Processamento interno de informações no sistema de IA de forma não transparente na tela, demandando indicadores visuais claros em tempo real)
- **4. Validação Cruzada Híbrida** (O usuário alterna frequentemente entre as respostas geradas pela IA e buscas tradicionais para validar dados e garantir confiança)
- **5. Endpoint Sem Clique (Zero-Click) / Ação & Decisão** (A jornada é encerrada diretamente na interface de IA que resolveu a dúvida ou avança para uma ação de conversão final altamente direcionada)

---
BRIEFING DO PROJETO:
[Insira aqui a descrição do produto ou serviço, as regras de negócio e os objetivos principais]

PERSONA ALVO:
[Insira aqui os dados da Persona, utilizando um nome realista, cargo de mercado específico e seu contexto operacional]

DADOS DE PESQUISA REAL:
[Cole aqui transcrições de entrevistas qualitativas, logs de suporte de sistemas legados, pesquisas de satisfação ou feedbacks de campo]
```

## Como usar

1. Gere primeiro a persona com o prompt de [Geração de persona](geracao-de-persona.md) e valide na [Auditoria](auditoria-de-persona.md) — depois cole os dados no bloco `PERSONA ALVO`.
2. Preencha `BRIEFING DO PROJETO` e `DADOS DE PESQUISA REAL` com material concreto.
3. **Escolha uma** das fases: **Opção A** (SaaS tradicional) ou **Opção B** (era da IA / busca generativa) — apague a que não usar.
4. Exija que a saída venha só como **tabela Markdown**, em prosa contínua nas células (sem bullets).

## Por que funciona

As **regras de controle** replicam a lógica anti-alucinação das personas na escala da jornada: pilha de ferramentas coesa, metas quantificáveis com prazo, dores operacionais em sistemas reais, e o **espaço negativo** (o que a persona rejeita). A exigência de **prosa contínua** e de **curva emocional justificada** evita o mapa raso de bullets, e as **oportunidades de design** ficam amarradas a gargalos concretos — virando insumo real de interface, não decoração.

## Relacionados

- [Geração de persona](geracao-de-persona.md) · [Auditoria de persona](auditoria-de-persona.md)
- Framework [CARE](../frameworks/01-ux-ui/CARE.md) (pesquisa) · princípio Flow Mode em [Visão geral](sobre.md)

---

[← Índice](../README.md) · [Visão geral da coleção](sobre.md)
