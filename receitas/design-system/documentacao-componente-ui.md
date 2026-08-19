---
titulo: Documentação de Componente de UI
tarefa: Design System
frameworks: [RTCF]
tecnicas: [Few-Shot]
nivel: Intermediário
---

# Documentação de Componente de UI

> Gera a especificação técnica de um componente **copiando exatamente** a sintaxe, os tokens e as regras de acessibilidade do seu Design System.

| | |
|---|---|
| **Tarefa** | Design System |
| **Framework** | [RTCF](../../frameworks/01-ux-ui/RTCF.md) |
| **Técnica** | [Few-Shot](../../tecnicas/few-shot.md) |
| **Nível** | Intermediário |

---

## 🎯 Objetivo

Garantir **consistência absoluta** ao alimentar um Design System. Combina o **RTCF** (Role, Task, Context, Format) com **Few-Shot** (exemplos estruturados de entrada→saída) para alinhar a IA às especificações exatas de código e acessibilidade da empresa.

## 🧩 Framework + Técnica

O **RTCF** define o papel (engenheiro de Design System), a tarefa e o formato. O **Few-Shot** faz o trabalho pesado: ao ver 2 componentes já documentados no padrão da casa, o modelo **replica a terminologia e a estrutura** em vez de inventar as suas.

## 📋 O Prompt

```text
#### ROLE (Papel)
Você é um Engenheiro de Design System especialista em acessibilidade digital (WCAG 2.2 AA) e desenvolvimento React/Tailwind.

#### TASK (Tarefa)
Gere a especificação técnica visual e de interação para o componente "Alert Banner" (Banner de Alerta do Sistema).

#### CONTEXT (Contexto)
Nosso produto é um dashboard corporativo B2B. Nosso design system utiliza tokens semânticos estritos para cores (os valores primitivos de cores já estão definidos, precisamos apenas do mapeamento funcional) e regras de foco consistentes para navegação via teclado.

#### FORMAT (Formato)
Utilize exatamente a estrutura demonstrada nos exemplos abaixo. Forneça o mapeamento de anatomia, os tokens de estilo e as regras de usabilidade.

---
#### EXEMPLO 1: Componente "Badge"
- **Anatomia:** Container retangular com cantos arredondados, ícone opcional à esquerda, rótulo de texto ao centro.
- **Tokens de Cor Semânticos:**
  * Sucesso: Fundo `bg-success-subtle`, Texto `text-success-depth`, Ícone `fill-success-depth`
- **Acessibilidade:** Elemento puramente informativo. Contraste mínimo de 4.5:1 atingido.

#### EXEMPLO 2: Componente "Button"
- **Anatomia:** Container interativo, ícone à esquerda (opcional), rótulo de texto, ícone à direita (opcional).
- **Tokens de Cor Semânticos:**
  * Primário (Ativo): Fundo `bg-primary-default`, Texto `text-on-primary`
  * Primário (Foco): Borda de foco externa `ring-focus-ring` (offset de 2px).
- **Acessibilidade:** Navegável via tecla `Tab`. Ativação via teclas `Enter` ou `Espaço`. Atributo `aria-disabled` dinâmico.

---
#### SUA TAREFA: Componente "Alert Banner" (Gere a partir daqui seguindo o formato acima)
- **Anatomia:** ...
- **Tokens de Cor Semânticos (Estados: Informação, Sucesso, Alerta Crítico):** ...
- **Acessibilidade (incluindo comportamento de leitores de tela/aria-live e foco):** ...
```

## ▶️ Como usar

1. Substitua os **dois exemplos** por componentes reais já documentados no seu Design System (quanto mais fiéis, melhor).
2. Troque o **componente-alvo** ("Alert Banner") pelo que você quer documentar.
3. Ajuste o **CONTEXT** para sua stack (React/Tailwind, Vue, tokens próprios etc.).
4. Reaproveite o mesmo prompt para documentar toda a biblioteca — a saída sai padronizada.

## 💡 Por que funciona

O aprendizado no contexto (*in-context learning*) via **Few-Shot** é a técnica mais eficaz para forçar a IA a copiar uma **sintaxe técnica complexa** e seguir a **terminologia própria da empresa**, eliminando desvios estéticos e alucinações de código.

## 🔁 Variações

- **Saída em código:** peça no FORMAT o componente em React + Tailwind, não só a spec.
- **Auditoria:** inverta — dê o componente pronto e peça para verificar aderência ao padrão dos exemplos.
- **Rigor de acessibilidade:** adicione um passo de [autocrítica](../../tecnicas/autocritica.md) checando WCAG 2.2 AA.

## 🔗 Relacionados

- Framework: [RTCF](../../frameworks/01-ux-ui/RTCF.md)
- Técnica: [Few-Shot](../../tecnicas/few-shot.md)

---

📚 [← Índice](../../README.md)
