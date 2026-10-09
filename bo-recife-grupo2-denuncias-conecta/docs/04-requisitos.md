# 04 — Requisitos

## Requisitos funcionais

| ID | Requisito | Origem | Prioridade |
| -- | --------- | ------ | ---------- |
| RF01 | O sistema deve permitir registrar uma denúncia com descrição, categoria informada, localização e data do fato | F1 | Alta |
| RF02 | O sistema deve permitir denúncia anônima | F1 | Alta |
| RF03 | O sistema deve gerar um protocolo único por denúncia | F2 | Alta |
| RF04 | O sistema deve sugerir categoria e órgão competente com base em regras | F3 | Alta |
| RF05 | O sistema deve sinalizar denúncias potencialmente duplicadas | F4 | Alta |
| RF06 | O atendente deve poder vincular denúncias duplicadas a um caso principal | F4 | Alta |
| RF07 | O atendente deve poder confirmar ou alterar o órgão sugerido | F5 | Alta |
| RF08 | O sistema deve registrar o histórico de status de cada denúncia | F5 | Alta |
| RF09 | O usuário deve poder consultar o status pelo protocolo | F6 | Média |
| RF10 | O gestor deve visualizar indicadores consolidados | F7 | Média |
| RF11 | O sistema deve importar denúncias a partir de CSV | F8 | Média |

## Requisitos não funcionais

| ID | Requisito | Critério de aceite |
| -- | --------- | ------------------ |
| RNF01 | Usabilidade: triagem em poucos passos | Registrar e encaminhar em até 5 interações |
| RNF02 | Desempenho | Resposta de tela em até 2 s com 1.000 registros de teste |
| RNF03 | Segurança e LGPD | Sem dados reais no repositório; campos pessoais opcionais; sigilo do denunciante preservado |
| RNF04 | Rastreabilidade | Toda mudança de status registra data e responsável |
| RNF05 | Explicabilidade | O sistema mostra qual regra gerou a sugestão de órgão |
| RNF06 | Portabilidade | Execução local com instruções no README |
| RNF07 | Acessibilidade | Interface responsiva e com contraste adequado |

## Regras de negócio

- RN01: Denúncia anônima não exibe dados do denunciante a nenhum perfil.
- RN02: A sugestão automática nunca encaminha sozinha; exige confirmação humana.
- RN03: Duas denúncias são "potencialmente duplicadas" quando têm categoria igual, local próximo e texto similar acima de um limiar configurável.
- RN04: Denúncia vinculada preserva o protocolo próprio e aponta para o caso principal.

## Rastreabilidade (resumo)

| Problema (docs/02) | Funcionalidade | Requisitos |
| ------------------ | -------------- | ---------- |
| Formulários distintos | F1, F8 | RF01, RF02, RF11 |
| Sem identificador único | F2, F4 | RF03, RF05, RF06 |
| Triagem manual | F3, F5 | RF04, RF07 |
| Acompanhamento disperso | F6, F7 | RF08, RF09, RF10 |
