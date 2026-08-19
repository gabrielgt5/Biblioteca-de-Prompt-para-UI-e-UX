# Autocrítica (Self-Refine) — O modelo revisa a si mesmo

> Antes de entregar, o modelo **testa a própria proposta** contra critérios explícitos (usabilidade, acessibilidade, estados de erro) e corrige o que falhou. É o diferencial do framework [C-C-E-R-A](../frameworks/01-ux-ui/C-C-E-R-A.md).

| | |
|---|---|
| **Tipo** | Técnica de verificação |
| **Melhor para** | Garantir qualidade técnica sem revisão manual: acessibilidade, heurísticas, robustez lógica |
| **Combina bem com** | [C-C-E-R-A](../frameworks/01-ux-ui/C-C-E-R-A.md) · [Prompting iterativo](prompting-iterativo.md) |

---

## O que é

Você adiciona uma etapa em que o modelo **avalia a saída que acabou de produzir**, lista os problemas encontrados e entrega uma versão corrigida — junto de um resumo do que ajustou. Neutraliza os erros mais comuns de geração de UI: contêineres vazios, falta de hierarquia e falhas de lógica entre estados.

## Quando usar

- O custo de um erro de UI/copy é alto e você **não pode revisar tudo manualmente**.
- Acessibilidade e conformidade (WCAG, heurísticas) precisam ser **garantidas**, não sugeridas.
- Como **passo final** de um fluxo [iterativo](prompting-iterativo.md).

## Como aplicar

```text
Antes da resposta final, execute uma autocrítica:
1. Teste contra [heurísticas de Nielsen / critérios de acessibilidade cognitiva].
2. Verifique [contraste AA, foco, rótulos para leitor de tela, estados vazio/erro/loading].
3. Aponte palavras/decisões que gerem ansiedade, ambiguidade ou fricção.
4. Corrija os problemas e entregue: (a) resumo do que ajustou + (b) a versão final consolidada.
```

## Exemplo (aplicado a UX)

No turno 3 do refino de microcopy de erro: *"Analise as mensagens contra acessibilidade cognitiva (a pessoa sob estresse entende o que fazer?) e sinalize palavras que causem ansiedade; apresente a versão consolidada final."* Veja [Microcopy de erro crítico](../receitas/ux-writing/microcopy-erro-critico.md).

## Armadilhas

- **Exija o relatório** das correções — sem isso, o modelo tende a pular a etapa.
- Dê **critérios concretos** (heurísticas, WCAG); "revise se está bom" produz autocrítica vazia.

---

📚 [← Índice](../README.md) · Relacionadas: [C-C-E-R-A](../frameworks/01-ux-ui/C-C-E-R-A.md) · [Prompting iterativo](prompting-iterativo.md)
