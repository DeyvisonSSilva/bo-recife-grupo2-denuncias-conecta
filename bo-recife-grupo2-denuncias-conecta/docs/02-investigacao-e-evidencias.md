# 02 — Investigação e Evidências

> **Regra do projeto:** nenhuma afirmação sem evidência. Abaixo, o que já foi levantado em fontes públicas e o que o grupo ainda precisa coletar.

## 1. Evidências já levantadas (fontes públicas)

| # | Evidência | Fonte | Relação com o problema |
| - | --------- | ----- | ---------------------- |
| E1 | O Conecta Recife tem categoria "Ouvidoria e Denúncias" com serviços separados: denúncia ao Procon, reclamação à Ouvidoria, Espaço Conecta/Ouvidoria | Portal Conecta Recife (conecta.recife.pe.gov.br/categoria/12) | Vários serviços/formulários para demandas semelhantes |
| E2 | A denúncia à Ouvidoria da Educação é feita por e-mail ou telefone, em horário restrito (07h–17h, seg–sex) | Portal Conecta Recife (serviço 593) | Canal paralelo ao app, com acompanhamento "via telefone" |
| E3 | A EMPREL gere a plataforma e os dados; os órgãos atendem a demanda conforme a natureza | Política de Segurança e Privacidade do Conecta Recife App (EMPREL) | Entrada centralizada, tratamento descentralizado |
| E4 | A Prefeitura já reconhece a dispersão de canais: o projeto Ouvidoria 4.0 cruza dados da Ouvidoria Geral, Conecta Recife e Ouvidoria SUS para análise de sentimento | Notícia, Prefeitura do Recife (jun/2024) | Confirma que existem bases separadas por canal |
| E5 | O app permite anexar fotos e acompanhar solicitações com notificação a cada mudança de etapa | Ficha do app na Google Play | Existe acompanhamento, mas por solicitação, não por caso consolidado **[VALIDAR]** |
| E6 | Teleatendimento, e-mail da Ouvidoria e atendimento presencial coexistem com o app | Site da Ouvidoria (ouvidoria.recife.pe.gov.br) | Múltiplos canais de entrada |

## 2. Evidências a coletar pelo grupo

| # | Ação | Responsável | Status |
| - | ---- | ----------- | ------ |
| C1 | Ler a descrição completa do desafio no Banco de Oportunidades e registrar os trechos relevantes |
| C2 | Percorrer o fluxo de denúncia no portal/app e registrar com prints em `assets/` |
| C3 | Entrevistar ao menos 3 pessoas que já fizeram denúncia/reclamação (roteiro abaixo) |
| C4 | Contatar a Ouvidoria/SCTI para entender o fluxo interno (se possível) |
| C5 | Consultar dados abertos de manifestações (portal de dados abertos do Recife) e documentar em `data/` |

### Roteiro de entrevista (cidadão)

1. Você já registrou denúncia ou reclamação à Prefeitura? Por qual canal?
2. Recebeu protocolo? Conseguiu acompanhar?
3. Quanto tempo levou para ter retorno?
4. Teve de repetir a denúncia em outro canal?
5. O que facilitaria o acompanhamento?

## 3. Análise de causas (hipóteses a validar)

```
EFEITO: tratamento fragmentado das denúncias
├── Canais: app, portal, telefone, e-mail, presencial
├── Processos: formulários e serviços separados por tema/órgão
├── Dados: bases por canal e por órgão, sem identificador único do caso
├── Pessoas: triagem manual e dependente do atendente
└── Tecnologia: ausência de camada comum de classificação e roteamento
```

## 4. Consequências (hipóteses a validar)

- Retrabalho de triagem e reclassificação
- Duplicidade de registros sobre o mesmo fato
- Demora no encaminhamento ao órgão competente
- Baixa transparência para o cidadão
- Dificuldade de análise gerencial consolidada

## 5. Como o problema é tratado hoje

Fluxo atual simplificado (a confirmar com C2 e C4):

```
Cidadão → (app | portal | 0800 | e-mail | presencial)
        → formulário/serviço específico
        → órgão responsável pela natureza da demanda
        → resposta/acompanhamento por canal e órgão
```

## 6. Lacunas

Sem dados quantitativos oficiais sobre volume de denúncias, taxa de duplicidade e tempo de encaminhamento, o grupo **não deve citar números** sem fonte. Se não forem obtidos, usar dados sintéticos declarados como tal em `data/README.md`.
