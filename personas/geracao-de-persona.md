# Geração de Persona (fundamentada em dados)

> Gera personas de UX **ancoradas em transcrições de pesquisa**, com dados concretos, sem alucinações, e coerentes ao longo da jornada (Flow Mode). A saída sai em **JSON mapeando restrições de layout** — pronta para virar decisão de design.

## Objetivo

Transformar dados brutos de pesquisa em uma persona **específica e verificável**, evitando os erros clássicos de persona gerada por IA (perfis genéricos, números arredondados, ausência de fricção real). O foco não é uma "bio bonita", mas **restrições de design mensuráveis**.

## O Prompt

Cole suas transcrições em `[INPUT_DADOS]` e rode.

```text
[SYSTEM_ROLE]
Atue como um Arquiteto de UX/UI Enterprise especialista em pesquisa de usuário.
Gere personas fundamentadas nos dados fornecidos — nunca em suposições ou médias genéricas.

[INPUT_DADOS]
<Insira aqui as transcrições de pesquisa, entrevistas ou dados brutos>

[DADOS CONCRETOS OBRIGATÓRIOS]
Para cada persona, especifique com precisão:
- Cargo e senioridade específicos (ex.: "Analista de CX pleno", não "profissional de suporte").
- Momento real da empresa (ex.: startup série B escalando o time de atendimento).
- Hub de ferramentas do dia a dia (as ferramentas que a pessoa realmente abre todos os dias).
- Contexto de trabalho (ambiente, pressões, quem cobra o quê, como o sucesso é medido).

[REGRAS_DE_GERAÇÃO]
1. Zero perfis genéricos ou "usuário médio". Se os dados não sustentam algo, escreva "dado insuficiente" — não invente.
2. Defina os limites de carga cognitiva (alta/baixa) da persona em cada etapa da jornada.
3. Especifique a modalidade de interação dominante (ex.: teclado vs. touch vs. voz).
4. Liste as dores como gargalos de fluxo de trabalho MENSURÁVEIS (tempo perdido, nº de cliques, retrabalho) — não adjetivos vagos.

[ANTI-ALUCINAÇÃO — corrija antes de entregar]
- Números arredondados: dados reais são assimétricos. Evite "30 anos e exatamente 5 de experiência".
- Falta de espaço negativo: usuários reais REJEITAM coisas. Inclua o que a persona NÃO quer, resiste ou ignora.
- Viés visual/estereótipo: não reforce clichês baseados em cargo, gênero ou setor.

[FLOW MODE]
Trate a persona como um token semântico contínuo: densidade de informação, acessibilidade e
modalidade de interação devem PERSISTIR e ser coerentes em toda a jornada. Gere um "filme"
consistente da pessoa em uso, não "fotos" isoladas que se contradizem entre telas.

[OUTPUT]
Responda em JSON, mapeando a persona em restrições de layout:
{
  "persona": {
    "nome": "",
    "cargo": "",
    "senioridade": "",
    "empresa_momento": "",
    "contexto_de_trabalho": ""
  },
  "ferramentas_diarias": [""],
  "carga_cognitiva": { "padrao": "alta|baixa", "picos": [""] },
  "modalidade_interacao": "teclado|touch|voz|híbrida",
  "dores": [
    { "descricao": "", "gargalo_mensuravel": "" }
  ],
  "rejeicoes": [""],
  "restricoes_de_layout": [""]
}
```

## Como usar

1. **Cole os dados** reais de pesquisa em `[INPUT_DADOS]` (quanto mais transcrição, melhor).
2. Ajuste os **DADOS CONCRETOS** ao seu setor, se precisar de campos extras.
3. Rode e depois **audite** a saída com a [Auditoria de persona](auditoria-de-persona.md).
4. Use o campo `restricoes_de_layout` como ponte direta para decisões de UI (densidade, tamanho de alvo, atalhos).

## Por que funciona

- **Ancoragem em dados** (`[INPUT_DADOS]`) impede o "usuário médio" inventado.
- As **regras negativas** (anti-alucinação) forçam assimetria, fricção e ausência de estereótipo — os três sinais de persona real.
- O **Flow Mode** garante coerência ao longo da jornada, não personas que se contradizem entre telas.
- A **saída em JSON de restrições** transforma a persona em insumo de design, não num texto decorativo.

## Relacionados

- [Auditoria de persona](auditoria-de-persona.md) — valide antes de confiar.
- Combina com o framework [CARE](../frameworks/01-ux-ui/CARE.md) (pesquisa) e a técnica [Autocrítica](../tecnicas/autocritica.md).

---

[← Índice](../README.md) · [Visão geral da coleção](sobre.md)
