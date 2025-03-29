# Preocupações Éticas em Engenharia de Software

Este documento lista preocupações éticas relevantes ao desenvolvimento de software, especialmente em projetos que envolvem Inteligência Artificial, LLMs, dados sensíveis e automação de processos públicos, como no caso da Secretaria de Segurança Pública (SSP-GO).

---

## 1. Privacidade e Proteção de Dados Pessoais
- **Risco:** Vazamento de dados sensíveis (ex: registros criminais, dados pessoais).
- **Impacto:** Violações da LGPD; danos à reputação institucional; prejuízos à privacidade.
- **Ação:** Criptografia, anonimização, controle de acesso, conformidade com a LGPD.

## 2. Segurança da Informação
- **Risco:** Invasões, vazamento de informações, adulteração de dados.
- **Impacto:** Perda de confiança no sistema, prejuízos operacionais.
- **Ação:** Auditorias, firewalls, autenticação forte, logs de acesso e segurança.

## 3. Transparência e Auditabilidade
- **Risco:** Decisões do sistema de IA serem opacas (*black box*).
- **Impacto:** Dificuldade para justificar decisões ou atender a auditorias.
- **Ação:** Garantir explicabilidade (XAI), manter logs acessíveis e compreensíveis.

## 4. Viés e Discriminação Algorítmica
- **Risco:** Dados enviesados levando a decisões injustas ou discriminatórias.
- **Impacto:** Violações de direitos; descrédito da tecnologia.
- **Ação:** Auditoria de viés, validação estatística, técnicas de fairness.

## 5. Consentimento Informado
- **Risco:** Uso de dados sem ciência ou permissão dos envolvidos.
- **Impacto:** Ilegalidade no uso de dados; quebra de confiança.
- **Ação:** Garantir uso de dados com base legal e consentimento quando aplicável.

## 6. Responsabilidade pelas Decisões do Sistema
- **Risco:** Falta de clareza sobre quem responde por erros do sistema.
- **Impacto:** Dificuldade em atribuir responsabilidades legais e técnicas.
- **Ação:** Definir responsáveis humanos por decisões e supervisão de IA.

## 7. Resistência e Impacto no Trabalho Humano
- **Risco:** Substituição de atividades humanas sem plano de transição.
- **Impacto:** Resistência de usuários; perda de conhecimento institucional.
- **Ação:** Planejamento de mudança, capacitação contínua, escuta ativa de usuários.

## 8. Sustentabilidade e Manutenção do Sistema
- **Risco:** Soluções que não são mantidas ou escaláveis.
- **Impacto:** Abandono do sistema, perda de recursos investidos.
- **Ação:** Boas práticas de engenharia (documentação, testes, versionamento, governança de dados).

## 9. Uso Indevido ou Malicioso da Tecnologia
- **Risco:** Uso do sistema para finalidades abusivas (ex: vigilância excessiva).
- **Impacto:** Riscos sociais, éticos e legais.
- **Ação:** Definição clara de escopo, monitoramento de uso, políticas de acesso e limites técnicos.

## 10. Qualidade e Completude dos Dados
- **Risco:** Decisões com base em dados incompletos, inconsistentes ou desatualizados.
- **Impacto:** Resultados imprecisos, falhas na geração de respostas ou relatórios.
- **Ação:** Monitoramento da qualidade dos dados, processos de ETL robustos, validações automatizadas.

---

> **Nota:** Este checklist pode ser expandido conforme novas demandas e riscos sejam identificados ao longo do ciclo de vida do projeto.
