# 06 — Arquitetura e Tecnologias

> Proposta inicial; o grupo deve ajustar conforme seu domínio de cada tecnologia.

## Arquitetura

```
[Formulário Web]   [Importador CSV]
        \             /
         ▼           ▼
      API REST (Python / FastAPI)
   ┌──────────┬──────────────┬──────────────┐
   │ Validação │ Classificador │ Detector de   │
   │ e padroni-│ (regras)      │ duplicidade   │
   │ zação     │               │ (similaridade)│
   └──────────┴──────────────┴──────────────┘
                   │
                   ▼
            SQLite (denúncias, órgãos, histórico, vínculos)
                   ▲
                   │
      Interface web (Jinja2/HTML) — atendente, cidadão, gestor
```

## Tecnologias e justificativas

| Camada | Tecnologia | Justificativa |
| ------ | ---------- | ------------- |
| Backend | Python + FastAPI | Rápido de desenvolver, documentação automática da API |
| Banco | SQLite | Sem servidor, adequado a MVP e fácil de executar |
| Similaridade | scikit-learn (TF-IDF) ou `difflib` | Simples, explicável, sem dependências pesadas |
| Interface | HTML + Jinja2 (ou React, se o grupo dominar) | Menor custo para fluxo ponta a ponta |
| Testes | pytest | Padrão em Python |
| Prototipação | Figma ou Penpot | Exigido na AV1 |
| Versionamento | Git/GitHub | Exigido pelo projeto |

## Modelo de dados (resumo)

| Tabela | Campos principais |
| ------ | ----------------- |
| denuncia | id, protocolo, descricao, categoria, localizacao, data_fato, anonima, canal_origem, orgao_sugerido, orgao_final, status, caso_principal_id |
| orgao | id, nome, palavras_chave |
| historico | id, denuncia_id, status, data, responsavel |

## Segurança e LGPD

Minimização de dados, anonimato opcional, dados sintéticos, nenhuma credencial no repositório, `.env.example` com valores fictícios.
