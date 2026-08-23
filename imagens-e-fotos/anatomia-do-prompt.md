# Anatomia de um Prompt de Imagem

> A fórmula que monta uma imagem intencional (e não genérica). Cada camada controla um aspecto do resultado — some as camadas na ordem e você tem um prompt completo.

## A fórmula

```text
[Sujeito] + [Composição] + [Iluminação] + [Textura] + [Equipamento Ótico]
```

| Camada | O que controla | Onde buscar vocabulário |
|---|---|---|
| **Sujeito** | O que é a imagem (quem/o quê + material/traço) | descreva com precisão |
| **Composição** | Enquadramento, ângulo e disposição | [Dicionário: Composição](dicionario-composicao.md) |
| **Iluminação** | A luz da cena e o clima | [Dicionário: Iluminação](dicionario-iluminacao.md) |
| **Textura** | O acabamento da superfície / mídia | [Dicionário: Texturas](dicionario-texturas.md) |
| **Equipamento Ótico** | A sensação de câmera/lente | `shot on 50mm f/1.4`, `macro`, `cinematic` |

E, opcionalmente, o **Estilo & Direção** (linguagem visual geral) — veja o [Dicionário: Estilos](dicionario-estilos.md).

## Exemplo montado

Cada anotação vira um trecho do prompt final:

- **Sujeito:** female cyborg, chrome plating
- **Composição:** dutch angle, off-center
- **Iluminação:** neon rim lighting, volumetric shadows
- **Textura:** authentic film grain, brushed metal
- **Equipamento:** shot on 50mm f/1.4, cinematic

Prompt completo (copiar):

```text
female cyborg, chrome plating, dutch angle off-center composition, neon rim lighting, volumetric shadows, authentic film grain, brushed metal texture, shot on 50mm f/1.4, cinematic
```

## Como usar

1. **Comece pelo Sujeito** — o que aparece e do que é feito.
2. **Adicione uma camada por vez** (composição → luz → textura → lente), copiando os fragmentos dos dicionários.
3. **Escreva os termos técnicos em inglês** — a maioria dos modelos responde melhor.
4. **Itere:** gere, veja o que faltou e ajuste só a camada fraca.
5. Se a ferramenta aceitar, use **negativos** (`no text, no watermark, no distorted hands`).

## Dicionários visuais

- [Iluminação](dicionario-iluminacao.md) — chiaroscuro, Rembrandt, high-key…
- [Composição](dicionario-composicao.md) — rule of thirds, knolling, dutch angle, isometric…
- [Texturas](dicionario-texturas.md) — impasto, film grain, matte ceramic, brushed metal…
- [Estilos & Direção](dicionario-estilos.md) — flat design, claymorphism, glassmorphism, editorial noir…
- [Catálogo por objetivo de negócio](catalogo-por-objetivo.md) — escolha o estilo pela meta.

---

[← Índice](../README.md) · [Visão geral da categoria](sobre.md)
