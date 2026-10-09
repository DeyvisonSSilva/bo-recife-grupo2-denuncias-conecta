# 07 — Planejamento do MVP

## Escopo do MVP

**Fluxo principal ponta a ponta:** registrar denúncia → protocolo → classificação sugerida → alerta de duplicidade → confirmação e encaminhamento → consulta por protocolo.

| Incluído | Fora do MVP |
| -------- | ----------- |
| F1, F2, F3, F4, F5, F6 | Integração real com EMPREL/Conecta |
| F8 (CSV) | Autenticação avançada por perfil |
| F7 em versão simples | Classificação por IA treinada |
| Dados sintéticos | Notificações push/e-mail |

## Cronograma sugerido (a ajustar às datas da disciplina)

| Semana | Entrega | Responsável |
| ------ | ------- | ----------- |
| 1 | Modelo de dados e esqueleto da API |
| 2 | F1, F2 (registro + protocolo) |
| 3 | F3 (classificação por regras) |
| 4 | F4 (duplicidade) e F5 (encaminhamento) |
| 5 | F6, F8, F7 simples |
| 6 | Testes, validação, métricas, documentação | Todos |

## Divisão de papéis (sugestão)

Backend/API · Interface · Dados e classificação · Testes e documentação. Todos devem ter commits próprios.

## Definição de pronto

Funcionalidade com código em `src/`, teste correspondente em `tests/`, documentada e executável pelo README.
