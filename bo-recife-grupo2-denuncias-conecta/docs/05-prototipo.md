# 05 — Protótipo

**Link público do protótipo navegável (Figma ou Penpot):** [PREENCHER]

## Telas previstas (mínimo necessário)

| Tela | Perfil | Função | Requisitos |
| ---- | ------ | ------ | ---------- |
| T1 Nova denúncia | Cidadão/Atendente | Formulário padronizado, opção anônima | RF01, RF02 |
| T2 Confirmação | Cidadão | Exibe protocolo gerado | RF03 |
| T3 Fila de triagem | Atendente | Lista pendentes com categoria e órgão sugeridos | RF04 |
| T4 Detalhe do caso | Atendente | Alerta de duplicidade, vincular, confirmar órgão, alterar status | RF05–RF08 |
| T5 Consulta por protocolo | Cidadão | Linha do tempo do caso | RF09 |
| T6 Painel | Gestor | Indicadores | RF10 |

## Fluxo navegável principal

```
T1 → T2 → T3 → T4 → T5
```

## Wireframe textual — T4 Detalhe do caso

```
┌──────────────────────────────────────────────┐
│ Protocolo: 2026-000123        Status: Em triagem │
├──────────────────────────────────────────────┤
│ Descrição: "..."                             │
│ Local: Boa Viagem        Data do fato: ...   │
├──────────────────────────────────────────────┤
│ Sugestão: Procon  (regra: "preço", "loja")   │
│ [Confirmar] [Alterar órgão ▼]                │
├──────────────────────────────────────────────┤
│ ⚠ Possível duplicidade com 2026-000098       │
│ [Vincular] [Não é duplicata]                 │
├──────────────────────────────────────────────┤
│ Histórico: recebido → classificado → ...     │
└──────────────────────────────────────────────┘
```

Capturas e exportações em `assets/`.
