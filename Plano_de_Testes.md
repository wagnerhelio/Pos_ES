# Plano de Teste

**Sistema:** Agente de Resposta LAI Automatizada  
**Versão:** 1.0

## Histórico das alterações

| Data       | Versão | Descrição       | Autor(a)         |
|------------|--------|------------------|------------------|
| 29/03/2025 | 1.0    | Release inicial  | Danielle Farias  |

---

## 1 - Introdução

Este plano de teste refere-se ao sistema de resposta automatizada a pedidos de acesso à informação (LAI), utilizando LLMs, integração de bases relacionais e NoSQL, e um fluxo de dados baseado no DW. A arquitetura foi implementada com uso de Django, Guardrails, Ollama e dashboards em Power BI/Qlik.

Objetivos:
- Validar a funcionalidade do pipeline de dados e da interface de requisição/resposta.
- Verificar consistência das respostas da LLM.
- Garantir integridade dos dados e segurança no processo.

---

## 2 - Requisitos a Testar

### Casos de uso:

| Identificador | Nome do caso de uso                          |
|---------------|-----------------------------------------------|
| UC01          | Receber requisição de LAI via interface web   |
| UC02          | Gerar prompt estruturado a partir da LAI      |
| UC03          | Traduzir prompt para SQL com Text2SQL         |
| UC04          | Executar consulta no DW (SQL e NoSQL)         |
| UC05          | Validar resposta com LLM Guardrails AI        |
| UC06          | Responder via canal (WhatsApp, Web, etc.)     |
| UC07          | Registrar logs de acesso e resposta           |

### Requisitos não-funcionais:

| Identificador | Nome do requisito                  |
|---------------|-------------------------------------|
| RNF01         | Tempo médio de resposta < 5s        |
| RNF02         | Taxa de erro nas respostas < 2%     |
| RNF03         | Log e auditoria de todas as ações   |
| RNF04         | Integração segura entre sistemas    |

---

## 3 - Tipos de Teste

- Teste de interface (Django e canais externos)
- Teste de integração (LLM + Guardrails + DW + API Text2SQL)
- Teste de segurança (controle de acesso, logs, prompt injection)
- Teste de performance (tempo de resposta da API e LLM)
- Teste de persistência (logs, requisições e respostas)
- Teste de aceitação (respostas corretas para LAIs reais e simuladas)

---

### 3.1 - API TextToSQL

- **Objetivo:** Verificar se os prompts são corretamente convertidos em SQL para o DW.
- **Técnica:** (x) Automática  
- **Estágio do teste:** Integração (x)  
- **Abordagem:** Caixa branca (x), Caixa preta (x)  
- **Responsáveis:** Equipe de backend/API

---

### 3.2 - Integração com DW (SQL/NoSQL)

- **Objetivo:** Validar se os dados são recuperados corretamente do DW.
- **Técnica:** (x) Manual / (x) Automática  
- **Estágio do teste:** Integração (x)  
- **Abordagem:** Caixa preta (x)  
- **Responsáveis:** DBA / Eng. de dados

---

### 3.3 - Validação com Guardrails AI

- **Objetivo:** Verificar se as respostas seguem políticas definidas e são auditáveis.
- **Técnica:** (x) Automática  
- **Estágio do teste:** Sistema (x)  
- **Abordagem:** Caixa preta (x)  
- **Responsáveis:** Cientista de dados / QA

---

### 3.4 - Interface Django / WhatsApp

- **Objetivo:** Garantir que a requisição da LAI e retorno de resposta estejam funcionais.
- **Técnica:** (x) Manual  
- **Estágio do teste:** Aceitação (x)  
- **Abordagem:** Caixa preta (x)  
- **Responsáveis:** QA / Time funcional

---

### 3.5 - Segurança e Logs

- **Objetivo:** Validar que os acessos e execuções estão sendo registrados de forma segura.
- **Técnica:** (x) Manual / (x) Automática  
- **Estágio do teste:** Sistema (x)  
- **Abordagem:** Caixa branca (x)  
- **Responsáveis:** DevSecOps / Backend

---

## 4 - Recursos

### 4.1 - Ambiente de Teste

- **Hardware:** Servidor Linux, 16GB RAM, 8 cores, GPU opcional.
- **Software:** PostgreSQL, MongoDB, Django, Power BI, Qlik, Ollama.

### 4.2 - Ferramentas de Teste

- Postman (API), Pytest, Selenium, JMeter, Guardrails AI, Prometheus (monitoramento).

---

## 5 - Cronograma

| Tipo de teste        | Duração  | Início      | Término     |
|----------------------|----------|-------------|-------------|
| Planejamento         | 2 dias   | 01/04/2025  | 02/04/2025  |
| Projetar testes      | 3 dias   | 03/04/2025  | 05/04/2025  |
| Implementar testes   | 4 dias   | 06/04/2025  | 09/04/2025  |
| Executar testes      | 5 dias   | 10/04/2025  | 15/04/2025  |
| Avaliar resultados   | 2 dias   | 16/04/2025  | 17/04/2025  |

---

> **Observação:** Este plano é baseado na arquitetura desenhada no projeto de automação de respostas LAI com uso de LLMs, frameworks locais e integração segura de dados. Ele será revisto a cada iteração.

