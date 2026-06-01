## Cover

# Agentes Pareceristas de Arquitetura

## Acelerando homologações com IA, governança e rastreabilidade

Everton R Martins

## Slide 1

# A homologação precisa escalar com segurança

Processos de homologação dependem de leitura técnica, evidências documentais e múltiplas áreas especialistas. O desafio é acelerar sem reduzir governança, segurança ou qualidade decisória.

- Documentos técnicos e comerciais chegam em formatos e níveis de maturidade diferentes.
- Arquitetura, segurança, dados, IA e negócio avaliam critérios complementares.
- A ausência de padronização aumenta tempo de ciclo e dificulta rastreabilidade.
- O objetivo é transformar análise documental em subsídio técnico consistente.

## Slide 2

# A solução apoia, não substitui, a decisão humana

Os agentes pareceristas são uma camada especializada de análise assistida por IA para organizar evidências, identificar lacunas e gerar pareceres técnicos após confirmação explícita do usuário.

- O agente analisa documentos, critérios e evidências.
- O humano revisa, decide e autoriza a geração do parecer.
- A emissão final depende de confirmação explícita.
- O processo institucional continua sendo a fonte de autoridade.

## Slide 3

# Cinco agentes cobrem os domínios críticos

A solução organiza a análise em cinco especialidades, permitindo avaliação técnica por domínio e consolidação de riscos para a homologação.

| Agente | Foco principal |
|---|---|
| Infraestrutura de TI | Disponibilidade, DR, conectividade, escalabilidade, observabilidade, backup e SLA. |
| Negócios e Soluções | Cobertura funcional, aderência técnica, escalabilidade e aderência ao negócio. |
| Segurança da Informação | Controles críticos, maturidade, riscos e evidências de segurança. |
| Arquitetura de Dados | Conformidade com requisitos de dados, IN 1431, IN 1432 e governança. |
| COE de IA | LLMs, RAG, MCP, A2A, IA Gateway, IA responsável e limites de autonomia. |

## Slide 4

# A jornada tem sete passos controlados

A experiência deve ser simples para o usuário e rigorosa para a governança. O fluxo separa autorização, análise prévia, revisão humana e emissão do parecer final.

| Etapa | Responsável | Resultado |
|---|---|---|
| Saudação e contexto | Usuário | Demanda caracterizada. |
| Envio de documentos | Usuário | Dossiê carregado. |
| Confirmação de análise | Usuário | Autorização registrada. |
| Análise prévia | Agente | Evidências, lacunas e riscos. |
| Revisão e decisão | Usuário | Aprovação, ajuste ou complementação. |
| Geração do parecer | Agente | Parecer técnico final. |
| Recebimento | Usuário | Parecer anexado ao processo. |

## Slide 5

# RAG torna o parecer mais rastreável

A arquitetura deve combinar modelos generativos com recuperação de conhecimento governado para reduzir respostas genéricas e fortalecer evidências.

- RAG conecta documentos, critérios, normas e checklists institucionais ao agente.
- O parecer deve distinguir evidência comprovada, lacuna documental e inferência.
- Versionamento da base de conhecimento é essencial para auditoria.
- A rastreabilidade aumenta confiança e reduz dependência de memória paramétrica do modelo.

## Slide 6

# Governança reduz riscos de IA generativa

Sistemas LLM exigem controles contra prompt injection, vazamento de dados, confiança excessiva, agência indevida e respostas sem sustentação documental.

| Risco | Controle essencial |
|---|---|
| Prompt injection | Separar instruções, conteúdo documental e comandos do usuário. |
| Vazamento de dados | Controle de acesso, classificação de informação e retenção segura. |
| Overreliance | Revisão humana obrigatória e mensagens claras de escopo. |
| Agência excessiva | Bloquear aprovação ou parecer final sem autorização explícita. |
| Alucinação | Exigir evidências, critérios e justificativa de maturidade. |

## Slide 7

# A matriz RACI clarifica responsabilidades

A governança operacional depende de explicitar quem executa, quem decide, quem consulta e quem deve ser informado em cada etapa.

| Etapa | Usuário | Agente | Especialistas | Comitê |
|---|---|---|---|---|
| Contextualizar demanda | R/A | I | I | I |
| Enviar documentos | R/A | I | C | I |
| Confirmar análise | R/A | I | C | I |
| Análise prévia | C | R | C | I |
| Revisar decisão | R/A | C | C | I |
| Gerar parecer | C | R | C | I |
| Registrar resultado | R | I | I | A/I |

## Slide 8

# O valor aparece em eficiência e qualidade

A solução deve ser medida por adoção, tempo de ciclo, completude de evidências, qualidade dos pareceres e redução de lacunas recorrentes.

- Redução do esforço manual de leitura preliminar.
- Padronização de critérios por domínio de arquitetura.
- Pareceres mais comparáveis, auditáveis e reutilizáveis.
- Dados para melhoria contínua de fornecedores, documentos e políticas.

## Slide 9

# O momento ideal é antes da decisão formal

Os agentes devem entrar quando existe dossiê documental mínimo e ainda há tempo para solicitar complementações, mitigar riscos e condicionar aprovação.

| Momento | Uso recomendado |
|---|---|
| Ideação | Uso parcial, sem parecer final. |
| RFI/RFP | Apoio exploratório e comparação inicial. |
| Dossiê recebido | Uso recomendado para análise estruturada. |
| Pré-comitê | Uso recomendado para subsidiar decisão. |
| Pós-contratação | Revisão, auditoria e melhoria contínua. |

## Slide 10

# O parecer deve ser padronizado

O template de parecer precisa permitir comparação entre homologações e reduzir ambiguidades técnicas.

- Identificação da solução, fornecedor, área solicitante e agente utilizado.
- Escopo, documentos avaliados, critérios aplicados e evidências encontradas.
- Lacunas, riscos, maturidade e recomendações objetivas.
- Conclusão com restrições, condicionantes e confirmação humana registrada.

## Slide 11

# A adoção exige comunicação institucional

A página no Confluence deve ser o ponto de entrada para explicar finalidade, acesso, agentes disponíveis, processo de uso, responsabilidades, limites e perguntas frequentes.

- Mostrar claramente quem deve usar e quando usar.
- Incluir link oficial do produto e orientações de acesso.
- Publicar exemplos de dossiê, critérios e perguntas frequentes.
- Reforçar que os agentes não substituem o processo de homologação.

## Slide 12

# Próximos passos recomendados

A evolução deve ocorrer por ciclos, começando por governança mínima e avançando para métricas, integração e melhoria contínua.

| Horizonte | Prioridade |
|---|---|
| Curto prazo | Formalizar templates, critérios, RACI e confirmação explícita. |
| Médio prazo | Integrar base governada, dashboards e versionamento de normas. |
| Longo prazo | Integrar ao workflow institucional com APIs, métricas e auditoria. |

## Slide 13

# Referências técnicas essenciais

A solução se fundamenta em boas práticas de IA generativa, RAG, governança, segurança LLM e privacidade.

- NIST AI Risk Management Framework: Generative AI Profile.
- ISO/IEC 42001:2023 para sistemas de gestão de IA.
- OWASP Top 10 for Large Language Model Applications.
- Lewis et al., Retrieval-Augmented Generation for Knowledge-Intensive NLP Tasks.
- Lei Geral de Proteção de Dados Pessoais e guias da ANPD.

## Slide 14

# Obrigado

Everton R Martins  
Email: engeverton@gmail.com  
Celular: +55 11 97690-9313  
LinkedIn: https://www.linkedin.com/in/everton-rubens-martins-366b86b4/
