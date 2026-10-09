# Painel Único de Denúncias - Conecta Recife

Projeto do **Grupo 2** para o desafio **"Fragmentação do Tratamento de Denúncias Recebidas via Conecta Recife"**, do Banco de Oportunidades (Coreto).

- **Instituição:** UNINASSAU, Campus Graças, Recife-PE
- **Curso:** Análise e Desenvolvimento de Sistemas (ADS)
- **Turma:** 5NNA
- **Disciplinas:** Ciência de Dados e Tópicos Integradores

## Sobre o projeto

As denúncias registradas no aplicativo Conecta Recife (buracos na via, iluminação pública, poda de árvores, descarte irregular de entulho, entre outras) são distribuídas entre diferentes secretarias sem um fluxo unificado de acompanhamento. Com isso, o cidadão perde a visibilidade do andamento do pedido, ocorre retrabalho entre órgãos e a gestão não consegue medir o tempo de resposta nem a taxa de resolução por tipo de ocorrência.

## Proposta de solução

O **Painel Único de Denúncias** é um módulo integrado ao Conecta Recife que funciona como um "hub": recebe a denúncia, gera um **protocolo único** automaticamente, classifica a categoria e a secretaria responsável e exibe uma linha do tempo de status visível para o cidadão e para os servidores:

**Recebida > Em análise > Encaminhada > Em execução > Concluída**

### Público-alvo

- **Cidadão do Recife**, que registra e acompanha ocorrências.
- **Servidor público** das secretarias responsáveis, que trata e resolve as demandas.

### Benefícios

- Maior transparência no acompanhamento das denúncias
- Redução do retrabalho entre órgãos
- Tempo de resposta mensurável para a gestão
- Mais confiança da população no canal oficial da Prefeitura

## Protótipo navegável (AV1)

- **Ferramenta:** Figma
- **Link:** [Protótipo navegável](https://www.figma.com/design/2mA6VnyXQidZMcTbvgkpsP/Coreto?node-id=0-1&t=nHQzZJgcv9IM7V9t-0)

**Jornada do usuário:**

Login/Splash do Conecta Recife > Nova Denúncia (categoria, localização no mapa e descrição com foto) > Confirmação com geração do Protocolo Único > Minhas Denúncias (lista com status) > Detalhe da Denúncia (linha do tempo e órgão responsável) > Notificação de Conclusão

## Planejamento para a AV2

O protótipo evoluirá para uma aplicação funcional, com as seguintes tecnologias previstas:

- **Back-end:** Node.js (Express) ou Java (Spring Boot)
- **Banco de dados:** PostgreSQL (denúncias, protocolo, status e histórico)
- **API REST:** classificação e encaminhamento automático à secretaria correspondente
- **Front-end:** React ou Flutter (web/mobile) para o cidadão
- **Painel administrativo web:** para os servidores atualizarem o status das demandas
- **Autenticação** de usuários
- **Notificações** (push/e-mail) sobre mudanças no andamento da denúncia

## Como executar

> Instruções serão adicionadas quando o código estiver disponível.

## Integrantes

| Nome | Matrícula |
|------|-----------|
| Deyvison Francisco | 01750371 |
| Augusto Alves | 01751499 |
| Adilson Pedro | 01751877 |
| Letícia Rodrigues | 01612042 |
| Pedro Lucas | 01750440 |

