# Auditoria de Persona (Anti-Viés e Anti-Alucinação)

> Checklist para **validar qualquer persona gerada por IA** antes de confiar nela. A IA produz perfis convincentes, mas muitas vezes falsos — este é o filtro.

## Bandeiras vermelhas (descarte se houver)

| Sinal de alerta | Por que é alucinação | O que o dado real parece |
|---|---|---|
| **Números arredondados** | A IA gera "30 anos exatos e exatamente 5 de experiência" | Dados reais são **assimétricos** (33 anos, 6 anos e 4 meses) |
| **Falta de espaço negativo** | A persona aceita qualquer recurso novo sem fricção | Usuários reais **rejeitam** mudanças complexas — deve haver o que ela evita |
| **Viés visual / estereótipo** | Imagens e traços reforçam clichês baseados em cargo | Pessoas reais **não** seguem o estereótipo do papel |

## O teste de estresse (checklist)

Passe a persona por estas três perguntas. Se falhar em qualquer uma, refine ou descarte:

- [ ] **Realismo populacional:** consigo encontrar 50 pessoas com este perfil exato no LinkedIn?
- [ ] **Durabilidade da dor:** a "dor" identificada sobrevive às próximas tendências de tecnologia, ou é passageira?
- [ ] **Coerência do ecossistema:** o hub de ferramentas faz sentido? (ex.: ninguém usa Salesforce **e** HubSpot para a exata mesma tarefa ao mesmo tempo)

## Prompt de auditoria (opcional)

Para rodar a auditoria sobre uma persona já gerada:

```text
Atue como um auditor cético de pesquisa de UX. Analise a persona abaixo e aponte alucinações.

[PERSONA]
<Cole aqui a persona gerada>

[AUDITORIA]
1. Bandeiras vermelhas: há números arredondados/simétricos? Falta espaço negativo (o que ela rejeita)? Há estereótipo de cargo?
2. Teste de estresse:
   - Existem 50+ pessoas com este perfil exato no LinkedIn?
   - A dor principal é estrutural (dura anos) ou passageira?
   - O ecossistema de ferramentas é coerente (sem redundâncias impossíveis)?
3. Veredito: APROVADA, ou REFINAR (liste exatamente o que corrigir), ou DESCARTAR (explique por quê).
Seja específico e implacável. É melhor descartar uma persona falsa do que projetar em cima dela.
```

## Por que funciona

Persona ruim custa caro: você projeta uma jornada inteira para alguém que não existe. As bandeiras vermelhas pegam os **artefatos típicos da IA** (simetria, ausência de fricção, estereótipo), e o teste de estresse checa se a persona **sobrevive ao mundo real** — população, durabilidade e coerência de ferramentas.

## Relacionados

- [Geração de persona](geracao-de-persona.md) — o prompt que já embute estas regras.
- Técnica: [Autocrítica](../tecnicas/autocritica.md).

---

[← Índice](../README.md) · [Visão geral da coleção](sobre.md)
