# Biblioteca de Prompts para UI e UX

Uma coletânea organizada para engenharia de prompt aplicada a UX/UI e design de produto, estruturada em **3 pilares**:

1. **Frameworks** — o *esqueleto* que organiza a intenção do prompt.
2. **Técnicas** — o *motor de raciocínio* que faz o modelo pensar melhor.
3. **Receitas** — a *entrega pronta*: framework × técnica aplicados a uma tarefa real.

> **A fórmula:** `Receita = Framework(s) × Técnica(s) aplicados a uma Tarefa de UX` — sempre com o "por que funciona".

> **Como usar:** identifique sua tarefa no [guia de escolha rápida](#-guia-de-escolha-rápida), abra o framework, a técnica ou a receita e copie o template.

---

## Frameworks

### Focados em UX/UI e Design
| Framework | Sigla | Melhor para |
|---|---|---|
| [CARE](frameworks/01-ux-ui/CARE.md) | Context, Ask, Rules, Examples | Planejamento de **pesquisa** e usabilidade (NN/g) |
| [RTCF](frameworks/01-ux-ui/RTCF.md) | Role, Task, Context, Format | **Alta fidelidade** e código semântico |
| [C-C-E-R-A](frameworks/01-ux-ui/C-C-E-R-A.md) | Clareza, Contexto, Especificidade, Ref. Visual, Autocrítica | Alta fidelidade com **acessibilidade e autocrítica** |
| [ICE](frameworks/01-ux-ui/ICE.md) | Instruction, Context, Expectation | Instruções **rápidas** do dia a dia |

### Corporativos e analíticos gerais
| Framework | Sigla | Melhor para |
|---|---|---|
| [COSTAR](frameworks/02-gerais/COSTAR.md) | Context, Objective, Style, Tone, Audience, Response | Alinhar **negócio ↔ design** |
| [CRISPE](frameworks/02-gerais/CRISPE.md) | Capacity, Insight, Statement, Personality, Experiment | Problemas **técnicos/analíticos** |
| [RACE](frameworks/02-gerais/RACE.md) | Role, Action, Context, Expectation | Entregas **rápidas e padronizadas** |
| [BAB](frameworks/02-gerais/BAB.md) | Before, After, Bridge | **UX Writing** e microcopy |

---

## Técnicas de prompting

| Técnica | O que faz | Melhor para |
|---|---|---|
| [Chain-of-Thought](tecnicas/chain-of-thought.md) | Raciocínio passo a passo antes de responder | Fluxos, arquitetura, decisões complexas |
| [Decomposição / Step Zero](tecnicas/decomposicao-step-zero.md) | Pensar a jornada antes das telas | Fluxos multi-tela (anti *screen myopia*) |
| [Few-Shot](tecnicas/few-shot.md) | Exemplos entrada→saída fixam a sintaxe | Design System, consistência |
| [Zero-Shot](tecnicas/zero-shot.md) | Instrução direta, sem exemplos | Tarefas simples e rápidas |
| [Prompting Iterativo](tecnicas/prompting-iterativo.md) | Refino conversacional v1→v2→v3 | Microcopy, refino cirúrgico |
| [Autocrítica](tecnicas/autocritica.md) | O modelo revisa a própria saída | Acessibilidade, qualidade técnica |

---

## Receitas (prompts aplicados por tarefa)

| Receita | Combinação | Tarefa |
|---|---|---|
| [Arquitetura de fluxo de onboarding](receitas/onboarding/arquitetura-fluxo-onboarding.md) | CARE × Chain-of-Thought | Onboarding |
| [Documentação de componente de UI](receitas/design-system/documentacao-componente-ui.md) | RTCF × Few-Shot | Design System |
| [Microcopy de erro crítico](receitas/ux-writing/microcopy-erro-critico.md) | C-C-E-R-A × Iterativo | UX Writing |
| [Mensagens de erro humanas (3 dimensões)](receitas/ux-writing/mensagens-erro-humanas.md) | RTCF × Few-Shot + Autocrítica | UX Writing |
| [Reescrita direta de microcopy (plug-and-play)](receitas/ux-writing/reescrita-direta-microcopy.md) | RTCF × Zero-Shot | UX Writing |

*Novas receitas por área (pesquisa, wireframe, acessibilidade, avaliação) serão adicionadas.*

---

## Prompt para imagem e fotos

Prompts para **gerar e editar imagens e fotos** com IA (Midjourney, DALL·E, Stable Diffusion, Gemini, Firefly).

| Página | Conteúdo |
|---|---|
| [Visão geral](imagens-e-fotos/sobre.md) | O que é, ferramentas comuns e boas práticas |
| [Anatomia do prompt](imagens-e-fotos/anatomia-do-prompt.md) | A fórmula (Sujeito + Composição + Iluminação + Textura + Equipamento) + exemplo montado |
| [Dicionário: Iluminação](imagens-e-fotos/dicionario-iluminacao.md) | Chiaroscuro, Rembrandt, High-Key |
| [Dicionário: Composição](imagens-e-fotos/dicionario-composicao.md) | Rule of Thirds, Knolling, Dutch Angle, Isometric 3D |
| [Dicionário: Texturas](imagens-e-fotos/dicionario-texturas.md) | Impasto, 35mm Film Grain, Matte Ceramic, Brushed Metal |
| [Dicionário: Estilos](imagens-e-fotos/dicionario-estilos.md) | Flat Design, Claymorphism, Glassmorphism, Editorial Noir |
| [Catálogo por objetivo](imagens-e-fotos/catalogo-por-objetivo.md) | Escolha o estilo visual pela meta de negócio |

---

## Personas

Prompts para **gerar e validar personas de UX** fundamentadas em dados reais (cargo, senioridade, momento da empresa, hub de ferramentas, contexto).

| Página | Conteúdo |
|---|---|
| [Visão geral](personas/sobre.md) | Dados concretos, Flow Mode e cuidado com IA |
| [Geração de persona](personas/geracao-de-persona.md) | Prompt principal: dados + anti-alucinação + Flow Mode + saída JSON |
| [Auditoria de persona](personas/auditoria-de-persona.md) | Bandeiras vermelhas e teste de estresse |
| [Mapa de Jornada do Usuário](personas/jornada-do-usuario.md) | Jornada detalhada em tabela, com regras de controle (SaaS ou era da IA) |

---

## Guia de escolha rápida

| Se você precisa... | Vá para |
|---|---|
| Planejar pesquisa de usuário / entrevista | **[CARE](frameworks/01-ux-ui/CARE.md)** |
| Desenhar uma tela/componente de alta fidelidade | **[RTCF](frameworks/01-ux-ui/RTCF.md)** |
| Garantir acessibilidade e autocrítica na UI | **[C-C-E-R-A](frameworks/01-ux-ui/C-C-E-R-A.md)** |
| Uma instrução rápida e pontual | **[ICE](frameworks/01-ux-ui/ICE.md)** |
| Conectar negócio ao design / falar com liderança | **[COSTAR](frameworks/02-gerais/COSTAR.md)** |
| Explorar soluções técnicas e comparar trade-offs | **[CRISPE](frameworks/02-gerais/CRISPE.md)** |
| Automatizar entregas repetitivas | **[RACE](frameworks/02-gerais/RACE.md)** |
| Escrever microcopy / mensagens de erro | **[BAB](frameworks/02-gerais/BAB.md)** |
| Estruturar um fluxo de onboarding completo | **[Receita: Onboarding](receitas/onboarding/arquitetura-fluxo-onboarding.md)** |
| Documentar componentes de um Design System | **[Receita: Design System](receitas/design-system/documentacao-componente-ui.md)** |
| Refinar mensagens de erro passo a passo | **[Receita: Microcopy](receitas/ux-writing/microcopy-erro-critico.md)** |

---

## Anatomia de um bom prompt

A maioria dos frameworks combina os mesmos ingredientes em proporções diferentes:

- **Papel/Role** — quem a IA encarna (especialista específico > genérico).
- **Contexto** — produto, usuário, restrições. É o campo que mais impacta a qualidade.
- **Tarefa/Ação** — o pedido claro e objetivo.
- **Regras/Restrições** — acessibilidade, tom, limites de negócio (as regras negativas "NUNCA…" direcionam muito).
- **Formato/Expectativa** — como você quer receber a saída.
- **Exemplos/Referência** — ancoram o padrão desejado ([Few-Shot](tecnicas/few-shot.md)).
- **Autocrítica** — o modelo revisa a si mesmo antes de entregar ([Autocrítica](tecnicas/autocritica.md)).

---

## Estrutura do repositório

```
.
├── README.md            ← você está aqui
├── index.html           ← viewer web (renderiza estes markdowns)
├── frameworks/
│   ├── 01-ux-ui/        CARE · RTCF · C-C-E-R-A · ICE
│   └── 02-gerais/       COSTAR · CRISPE · RACE · BAB
├── tecnicas/            Chain-of-Thought · Few-Shot · Zero-Shot · Iterativo · Autocrítica · Step Zero
├── receitas/
│   ├── onboarding/
│   ├── design-system/
│   └── ux-writing/
├── imagens-e-fotos/     Prompts para gerar e editar imagens e fotos
└── personas/            Prompts para gerar e validar personas de UX
```

---

*Biblioteca em construção — novas técnicas e receitas por tarefa serão adicionadas.*
