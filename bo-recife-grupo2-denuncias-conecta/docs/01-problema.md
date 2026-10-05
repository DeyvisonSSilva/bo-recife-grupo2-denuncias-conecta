# 01 — Problema

## 1. Desafio escolhido

**Fragmentação do Tratamento de Denúncias Recebidas via Conecta Recife.**
Link no Banco de Oportunidades: https://coreto.app.emprel.gov.br/banco-de-bo/fragmentacao-do-tratamento-de-denuncias-recebidas-via-conecta-recife

## 2. Descrição do problema

O Conecta Recife é a plataforma de serviços da Prefeitura, com aplicativo, portal web, teleatendimento (0800 281 0040) e atendimento presencial. Pelo portal, o cidadão encontra na categoria *Ouvidoria e Denúncias* serviços distintos, como denunciar estabelecimento ao Procon, registrar reclamação na Ouvidoria e denunciar ou reclamar à Ouvidoria da Educação.

A política de privacidade do app informa que a EMPREL gerencia a plataforma e armazena os dados, enquanto os **órgãos da administração direta e indireta** atendem a demanda conforme sua natureza. Ou seja, o ponto de entrada é único, mas **o tratamento é distribuído**.

**Fragmentação**, neste projeto, significa que a mesma denúncia, ou denúncias sobre o mesmo fato, pode:

- ser recebida por canais e formulários diferentes, com campos diferentes;
- ser encaminhada a órgãos diferentes sem uma visão consolidada do caso;
- gerar registros duplicados ou parcialmente sobrepostos;
- ter acompanhamento disperso, dificultando ao cidadão e à gestão saber o status real. **[VALIDAR com o texto oficial do BO e com a Ouvidoria]**

## 3. Quem é afetado

| Público | Como é afetado |
| ------- | -------------- |
| Cidadão denunciante | Não sabe para onde a denúncia foi nem em que etapa está; pode ter de repetir informações |
| Atendentes e ouvidores | Triagem manual, reclassificação, retrabalho com duplicidades |
| Órgãos responsáveis (Procon, secretarias, Emlurb etc.) | Recebem demandas incompletas ou fora da sua competência |
| Gestão municipal | Sem visão consolidada para priorizar, medir prazos e identificar padrões |

## 4. Delimitação (escopo do projeto)

**Dentro do escopo:** denúncias registradas via Conecta Recife; triagem, classificação, roteamento sugerido, detecção de duplicidade e acompanhamento unificado.

**Fora do escopo:** resolução do mérito da denúncia pelos órgãos; integração real com os sistemas internos da Prefeitura/EMPREL; reconhecimento automático por IA em produção; denúncias de assédio e corregedoria (fluxo sigiloso próprio).

## 5. Pergunta orientadora

> Como reduzir a fragmentação no tratamento de denúncias recebidas pelo Conecta Recife, de modo que cada denúncia tenha triagem padronizada, destino claro e acompanhamento único?
