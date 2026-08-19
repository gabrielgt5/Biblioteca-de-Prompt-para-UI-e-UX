# Few-Shot — Aprendizado por exemplos

> Você fornece **exemplos de entrada→saída** dentro do próprio prompt para o modelo copiar a sintaxe, a terminologia e o formato exatos. É a técnica mais eficaz para **consistência** e para eliminar alucinações de código/estrutura.

| | |
|---|---|
| **Tipo** | Técnica de contexto (*in-context learning*) |
| **Melhor para** | Alimentar Design Systems, gerar saídas com sintaxe/terminologia própria, padronizar documentação |
| **Combina bem com** | [RTCF](../frameworks/01-ux-ui/RTCF.md) · [COSTAR](../frameworks/02-gerais/COSTAR.md) |

---

## O que é

Em vez de **descrever** o formato desejado, você **demonstra** com 1–3 exemplos resolvidos. O modelo infere o padrão e o replica na sua tarefa real. "Few-shot" = poucos exemplos (1 = *one-shot*, 0 = [*zero-shot*](zero-shot.md)).

## Quando usar

- A saída precisa seguir uma **sintaxe técnica complexa** (tokens, nomenclatura interna, estrutura fixa).
- Você quer **consistência absoluta** entre itens gerados (ex.: cada componente do Design System documentado igual).
- Descrever o formato por texto seria ambíguo — mostrar é mais barato e preciso.

## Como aplicar

```text
Utilize exatamente a estrutura demonstrada nos exemplos abaixo.

### EXEMPLO 1: [item conhecido]
[saída ideal, no formato exato]

### EXEMPLO 2: [outro item conhecido]
[saída ideal, no formato exato]

---
### SUA TAREFA: [novo item]
[gere a partir daqui, seguindo o formato acima]
```

## Exemplo (aplicado a UX)

Documentar um componente "Alert Banner" fornecendo antes exemplos completos de "Badge" e "Button" — o modelo copia a anatomia, os tokens semânticos e as regras de acessibilidade. Veja a receita [Documentação de componente de UI](../receitas/design-system/documentacao-componente-ui.md).

## Armadilhas

- **Exemplos inconsistentes entre si** confundem o modelo — eles precisam ser fiéis ao padrão.
- Exemplos muito longos gastam tokens; use os **mínimos suficientes** para fixar o padrão.
- Se os exemplos tiverem um erro, o modelo **replica o erro**. Curadoria importa.

---

📚 [← Índice](../README.md) · Relacionadas: [Zero-Shot](zero-shot.md) · [Chain-of-Thought](chain-of-thought.md)
