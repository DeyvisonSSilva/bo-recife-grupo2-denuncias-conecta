# 08 — Testes e Validação

> **Status:** plano de testes definido para a AV2. Os resultados serão registrados após a implementação do MVP.

## Objetivo

Verificar se o fluxo principal do MVP funciona de ponta a ponta e se atende aos requisitos descritos em `04-requisitos.md`.

## Estratégia de testes

| Tipo | O que verifica |
| ---- | -------------- |
| Testes unitários | Geração de protocolo (F2), classificação por regras (F3) e detecção de duplicidade (F4) |
| Testes de integração | API e banco de dados: registro (F1), encaminhamento (F5) e consulta por protocolo (F6) |
| Teste de fluxo ponta a ponta | Registrar denúncia → protocolo → classificação sugerida → alerta de duplicidade → confirmação e encaminhamento → consulta |
| Validação com usuários | Uso do protótipo/MVP por colegas e pessoas de fora da turma, seguindo a jornada do cidadão |

## Casos de teste principais

| ID | Cenário | Entrada | Resultado esperado |
| -- | ------- | ------- | ------------------ |
| CT01 | Registrar denúncia válida (F1, F2) | Categoria, localização e descrição preenchidas | Denúncia salva e protocolo único gerado |
| CT02 | Registrar denúncia incompleta | Campo obrigatório vazio | Denúncia rejeitada com mensagem de erro e sem protocolo |
| CT03 | Classificação por regras (F3) | Descrição como "buraco na rua" | Categoria e secretaria responsável sugeridas corretamente |
| CT04 | Alerta de duplicidade (F4) | Denúncia semelhante na mesma região e categoria | Sistema exibe alerta de possível duplicidade |
| CT05 | Encaminhamento (F5) | Confirmação da denúncia | Status "Encaminhada" e órgão responsável registrado |
| CT06 | Consulta por protocolo (F6) | Protocolo existente e protocolo inexistente | Status e histórico exibidos; mensagem de "não encontrado" quando inválido |
| CT07 | Unicidade do protocolo | Várias denúncias registradas em sequência | Nenhum protocolo repetido |

## Dados de teste

Serão usados **dados sintéticos**, sem informações pessoais reais de cidadãos.

## Critérios de aceitação

Uma funcionalidade é considerada pronta quando possui código em `src/`, teste correspondente em `tests/` passando, documentação e execução possível pelo README (definição de pronto em `07-planejamento-do-mvp.md`).

## Validação com usuários

- **Roteiro:** pedir a 3 a 5 pessoas que registrem uma denúncia e depois consultem o andamento pelo protocolo.
- **Observações:** dificuldades encontradas, dúvidas e sugestões.
- **Métricas:** taxa de conclusão da tarefa, tempo para concluir e nota de facilidade de uso (1 a 5).
