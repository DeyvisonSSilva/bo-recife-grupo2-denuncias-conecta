# 03 — Proposta de Solução

## 1. Visão

**Denúncia Única Recife** (nome provisório): camada de triagem e acompanhamento unificado que recebe denúncias vindas do Conecta Recife, padroniza, classifica, sugere o órgão competente, sinaliza duplicidades e mantém um histórico único por caso.

## 2. Por que funcionaria

| Causa (docs/02) | Como a proposta ataca |
| --------------- | --------------------- |
| Formulários e campos diferentes | Modelo de dados padronizado e obrigatórios mínimos |
| Sem identificador único do caso | Protocolo único e vínculo entre denúncias do mesmo fato |
| Triagem manual | Classificação sugerida por regras (palavras-chave, categoria, localização) |
| Duplicidade | Detecção por similaridade de texto, local e período |
| Acompanhamento disperso | Linha do tempo única, consultável pelo protocolo |

## 3. Público-alvo

- **Primário:** atendente/ouvidor que faz a triagem.
- **Secundário:** cidadão denunciante (consulta de status) e gestor (painel).

## 4. Funcionalidades

| ID | Funcionalidade | Prioridade MVP |
| -- | -------------- | -------------- |
| F1 | Registrar denúncia (formulário padronizado, com anônimo opcional) | Alta |
| F2 | Gerar protocolo único | Alta |
| F3 | Classificar categoria e sugerir órgão competente | Alta |
| F4 | Detectar possíveis duplicidades e permitir vincular casos | Alta |
| F5 | Atribuir/encaminhar ao órgão e registrar mudança de status | Alta |
| F6 | Consultar andamento por protocolo | Média |
| F7 | Painel com indicadores (volume, duplicidades, tempo de triagem) | Média |
| F8 | Importar denúncias de arquivo CSV (simula canais diferentes) | Média |

## 5. Abordagem de classificação

Primeira versão **baseada em regras** (dicionário de palavras-chave por órgão/categoria), por ser simples, explicável e testável. Evolução futura: modelo de linguagem ou classificador treinado, só após validar com dados reais.

## 6. Premissas e riscos

| Risco | Mitigação |
| ----- | --------- |
| Sem acesso a dados reais | Dados sintéticos documentados em `data/` |
| Sem integração com sistemas da Prefeitura | MVP independente, com importação por CSV simulando entrada do Conecta |
| Dados pessoais (LGPD) | Minimização, anonimato opcional, nenhum dado real versionado |
| Classificação incorreta | A sugestão sempre passa por confirmação humana |

## 7. Fluxo principal do MVP

```
Denúncia chega (formulário/CSV)
   ↓
Sistema valida e padroniza
   ↓
Classifica e sugere órgão + checa duplicidade
   ↓
Atendente confirma e encaminha
   ↓
Protocolo e histórico atualizados
   ↓
Cidadão/gestor consulta status
```
