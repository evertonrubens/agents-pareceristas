# Referências validadas e achados técnicos para o documento dos Agentes Pareceristas

Este arquivo consolida fontes externas públicas utilizadas apenas para fundamentação técnica geral. O conteúdo confidencial enviado pelo usuário permanece restrito ao contexto desta tarefa e não é incorporado a estas fontes.

## Fontes oficiais, normativas e de segurança

| ID | Fonte | URL | Achados úteis para o documento |
|---|---|---|---|
| R1 | NIST AI RMF: Generative AI Profile (NIST AI 600-1) | https://www.nist.gov/publications/artificial-intelligence-risk-management-framework-generative-artificial-intelligence | Perfil oficial do NIST para riscos de IA generativa, companion do AI RMF 1.0, aplicável a governança, medição e mitigação de riscos em GenAI. |
| R2 | ISO/IEC 42001:2023 | https://www.iso.org/standard/42001 | Primeiro padrão internacional de sistema de gestão de IA; especifica requisitos para estabelecer, implementar, manter e melhorar continuamente um AI Management System; destaca transparência, rastreabilidade, confiabilidade, gestão de riscos e oportunidades. |
| R3 | OWASP Top 10 for Large Language Model Applications | https://owasp.org/www-project-top-10-for-large-language-model-applications/ | Lista riscos críticos de aplicações LLM, como prompt injection, insecure output handling, sensitive information disclosure, excessive agency e overreliance; útil para nota de controles e limites de autonomia. |
| R4 | Lei Geral de Proteção de Dados Pessoais, Lei nº 13.709/2018 | https://www.planalto.gov.br/ccivil_03/_ato2015-2018/2018/lei/l13709.htm | Define proteção de dados pessoais, fundamentos como privacidade e autodeterminação informativa, conceitos de dado pessoal, dado sensível, controlador, operador, tratamento e relatório de impacto. |
| R5 | ANPD — Guia orientativo de segurança da informação para agentes de tratamento | https://www.gov.br/anpd/pt-br/centrais-de-conteudo/materiais-educativos-e-publicacoes/guia-orientativo-sobre-seguranca-da-informacao-para-agentes-de-tratamento-de-pequeno-porte | Referência nacional para boas práticas de segurança da informação e registros de operações de tratamento, ainda que voltada a pequeno porte. |

## Fontes acadêmicas e técnicas sobre RAG, agentes e humano-no-loop

| ID | Fonte | URL | Achados úteis para o documento |
|---|---|---|---|
| R6 | Lewis et al. (2020), Retrieval-Augmented Generation for Knowledge-Intensive NLP Tasks | https://arxiv.org/abs/2005.11401 | RAG combina memória paramétrica de modelos com memória não paramétrica recuperável; melhora respostas em tarefas intensivas em conhecimento e apoia atualização/proveniência do conhecimento. |
| R7 | Agentic Retrieval-Augmented Generation: A Survey | https://arxiv.org/abs/2501.09136 | Agentic RAG integra agentes autônomos a pipelines RAG com reflexão, planejamento, uso de ferramentas e colaboração multiagente para workflows complexos e multietapas. |
| R8 | Survey on Evaluation of LLM-based Agents | https://arxiv.org/abs/2503.16416 | Agentes LLM são avaliados em dimensões como planejamento, uso de ferramentas, autorreflexão e memória; há lacunas críticas em custo-eficiência, segurança e robustez. |
| R9 | Alon-Barkat & Busuioc (2023), Human–AI Interactions in Public Sector Decision Making | https://academic.oup.com/jpart/article-abstract/33/1/153/6524536 | Discute vieses na interação humano-algoritmo, incluindo automação e adesão seletiva; reforça que sistemas de apoio à decisão não removem a responsabilidade humana. |

## Fontes Google Cloud/GCP aplicáveis à arquitetura conceitual

| ID | Fonte | URL | Achados úteis para o documento |
|---|---|---|---|
| R10 | Google Cloud — Choose your agentic AI architecture components | https://docs.cloud.google.com/architecture/choose-agentic-ai-architecture-components | Define componentes de arquitetura agentic: frontend, agent development framework, ferramentas, memória, padrões de design, runtime de agente, modelo e runtime de modelo; compara ADK, MCP, A2A, Cloud Run, GKE e Vertex AI Agent Engine. |
| R11 | Google Cloud — Vertex AI Agent Builder documentation | https://docs.cloud.google.com/agent-builder | Vertex AI Agent Builder ajuda desenvolvedores a construir, escalar e governar agentes de IA em produção. |
| R12 | Google Cloud — Retrieval-Augmented Generation use case | https://cloud.google.com/use-cases/retrieval-augmented-generation | RAG combina recuperação de informação e LLMs para outputs mais precisos, atualizados e aderentes ao domínio; destaca grounded output e métricas de avaliação como coerência, grounding, segurança e aderência às instruções. |
| R13 | Google Developers Blog — Vertex AI RAG Engine | https://developers.googleblog.com/en/vertex-ai-rag-engine-a-developers-tool/ | RAG Engine como serviço gerenciado de orquestração para recuperar informações e alimentar LLMs; destaca redução de alucinações, dados atualizados, domínio especializado e casos em serviços financeiros. |
