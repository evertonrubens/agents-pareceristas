# Diagramas editáveis — Agentes Pareceristas de Arquitetura

Este arquivo contém os diagramas em Mermaid para uso direto no Confluence, em Markdown ou em ferramentas compatíveis com Mermaid. Cada diagrama foi desenhado para ser facilmente editável e também pode ser renderizado como imagem PNG quando necessário.

## Diagrama 1 — Visão de arquitetura da solução

```mermaid
flowchart LR
    U[Usuário solicitante<br/>área demandante ou homologação] --> UI[Interface web<br/>Agentes Solucionadores de Arquitetura]
    UI --> AUTH[Autenticação e perfil de acesso]
    AUTH --> ORQ[Orquestrador conversacional<br/>controle de sessão e confirmação humana]

    ORQ --> DOC[Serviço de ingestão documental<br/>PDF DOCX TXT XLSX PNG JPG]
    DOC --> OCR[Extração textual/OCR<br/>normalização e metadados]
    OCR --> CLASS[Classificação documental<br/>técnico comercial evidências anexos]

    CLASS --> RAG[Camada RAG e base de conhecimento<br/>políticas critérios normas checklists]
    RAG --> A1[Agente Infraestrutura de TI]
    RAG --> A2[Agente Negócios e Soluções]
    RAG --> A3[Agente Segurança da Informação]
    RAG --> A4[Agente Arquitetura de Dados]
    RAG --> A5[Agente COE de IA]

    A1 --> SCORE[Motor de evidências e maturidade<br/>Alta Média Baixa]
    A2 --> SCORE
    A3 --> SCORE
    A4 --> SCORE
    A5 --> SCORE

    SCORE --> REVIEW[Revisão humana obrigatória<br/>decisão de gerar parecer]
    REVIEW -->|Confirmação explícita| PARECER[Geração do parecer técnico final]
    REVIEW -->|Sem confirmação| WAIT[Aguardando ajustes ou novos documentos]

    PARECER --> AUDIT[Histórico, trilha de auditoria<br/>métricas e observabilidade]
    AUDIT --> DASH[Dashboard de adoção, qualidade<br/>SLA e melhoria contínua]
```

## Diagrama 2 — Processo de uso em homologação

```mermaid
flowchart TD
    S0[Início da homologação<br/>parceiro produto sistema ou ferramenta] --> S1[1. Saudação inicial<br/>responsável: usuário]
    S1 --> S2[2. Envio dos documentos<br/>responsável: usuário]
    S2 --> S3[3. Confirmação para iniciar análise<br/>responsável: usuário]
    S3 -->|Confirma análise| S4[4. Análise prévia dos documentos<br/>responsável: agente]
    S3 -->|Não confirma| SA[Solicitar complementação<br/>ou encerrar sessão]
    S4 --> S5[5. Revisão e decisão<br/>responsável: usuário]
    S5 -->|Parecer aprovado para emissão| S6[6. Geração do parecer<br/>responsável: agente]
    S5 -->|Exige ajustes| S2
    S6 --> S7[7. Recebimento do parecer<br/>responsável: usuário]
    S7 --> S8[Registro no dossiê de homologação<br/>e encaminhamento ao processo decisório]
```

## Diagrama 3 — Integração funcional entre os cinco agentes

```mermaid
flowchart TB
    CASE[Dossiê de homologação<br/>documentos técnicos comerciais e evidências] --> TRIAGEM[Triagem e roteamento<br/>tipo de solução risco domínio e documentos]

    TRIAGEM --> INFRA[Infraestrutura de TI<br/>disponibilidade DR conectividade escalabilidade observabilidade backup SLA continuidade]
    TRIAGEM --> NEG[Negócios e Soluções<br/>cobertura escalabilidade aderência técnica e aderência ao negócio]
    TRIAGEM --> SI[Segurança da Informação<br/>21 controles críticos e maturidade]
    TRIAGEM --> DADOS[Arquitetura de Dados<br/>IN 1431 IN 1432 requisitos aplicáveis e conformidade]
    TRIAGEM --> COE[COE de IA<br/>LLM MCP A2A IA Gateway RAG governança e uso responsável]

    INFRA --> CONS[Consolidação de evidências]
    NEG --> CONS
    SI --> CONS
    DADOS --> CONS
    COE --> CONS

    CONS --> RISK[Mapa de riscos e lacunas]
    RISK --> REC[Recomendações e condicionantes]
    REC --> DEC[Subsídio ao comitê ou fluxo institucional de homologação]
```

## Diagrama 4 — Governança, segurança e limites de autonomia

```mermaid
flowchart LR
    POL[Políticas institucionais<br/>normas internas LGPD segurança IA responsável] --> KB[Base governada de conhecimento]
    KB --> RAG[RAG com recuperação rastreável]
    RAG --> AG[Agentes pareceristas]

    AG --> CTRL1[Controle 1<br/>não emitir parecer sem confirmação explícita]
    AG --> CTRL2[Controle 2<br/>evidências e citações documentais]
    AG --> CTRL3[Controle 3<br/>classificação de maturidade e justificativa]
    AG --> CTRL4[Controle 4<br/>logs métricas auditoria e observabilidade]
    AG --> CTRL5[Controle 5<br/>restrição de escopo e prevenção de uso indevido]

    CTRL1 --> HUM[Humano responsável pela decisão]
    CTRL2 --> HUM
    CTRL3 --> HUM
    CTRL4 --> GOV[Governança e melhoria contínua]
    CTRL5 --> GOV

    HUM --> PROC[Processo institucional de homologação]
    GOV --> PROC
```

## Diagrama 5 — Fluxo RAG, memória e parecer rastreável

```mermaid
sequenceDiagram
    participant Usuario as Usuário
    participant UI as Interface dos Agentes
    participant Ingestao as Ingestão Documental
    participant RAG as RAG/Base de Conhecimento
    participant Agente as Agente Especialista
    participant Humano as Revisão Humana
    participant Parecer as Parecer Final

    Usuario->>UI: Acessa o agente e contextualiza a necessidade
    Usuario->>Ingestao: Envia documentos técnicos e comerciais
    UI->>Usuario: Solicita confirmação explícita para iniciar análise
    Usuario->>UI: Confirma início da análise
    Ingestao->>RAG: Extrai texto, metadados e evidências relevantes
    RAG->>Agente: Recupera critérios, normas e referências aplicáveis
    Agente->>Agente: Analisa evidências, lacunas, riscos e maturidade
    Agente->>Humano: Apresenta análise prévia e recomendações
    Humano->>Agente: Aprova, ajusta ou solicita complementação
    Agente->>Parecer: Gera parecer somente após aprovação explícita
    Parecer->>Usuario: Entrega parecer técnico final rastreável
```

## Diagrama 6 — Mapa de valor para áreas usuárias

```mermaid
mindmap
  root((Agentes Pareceristas))
    Homologação
      Redução de tempo de análise
      Padronização de critérios
      Dossiê técnico mais completo
    Arquitetura
      Pareceres por especialidade
      Evidências e recomendações
      Maturidade Alta Média Baixa
    Governança
      Rastreabilidade
      Métricas e dashboards
      Auditoria e melhoria contínua
    Segurança
      Controles críticos
      LGPD e segurança da informação
      Limites de autonomia
    Estratégia
      Escala institucional
      Comunicação clara
      Apoio à tomada de decisão
```
