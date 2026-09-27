# Atividade 2: Organização da Qualidade no LocalEats

## 1. Identificação

**Turma:** 2026/2  
**Equipe:** Gabriel e William  




**Elemento de Competência:** Identificar papéis, responsabilidades e competências relacionadas às atividades de qualidade e testes.

---

## 2. Tarefa 1: Diagnóstico da situação

### 2.1 Problemas organizacionais

| Problema identificado | Possível consequência para o produto ou para a equipe |
|---|---|
| Ausência de critérios claros para considerar uma funcionalidade pronta. | Cada integrante pode adotar um entendimento diferente, gerando entregas incompletas, retrabalho e defeitos. |
| Qualidade e testes são tratados como responsabilidade exclusiva do QA. | O QA torna-se um gargalo, os defeitos aparecem tarde e a equipe perde oportunidades de prevenção. |
| Defeitos, responsáveis e decisões de liberação não são registrados de modo consistente. | Problemas podem ser esquecidos, correções perdem prioridade e a liberação deixa de ter uma decisão rastreável. |

### 2.2 Responsabilidade pela qualidade

**A qualidade do LocalEats deve ser responsabilidade exclusiva do profissional de QA? Justifiquem.**

Não. A qualidade deve ser responsabilidade de toda a equipe. William, como Product Owner, define prioridades, esclarece as necessidades do produto e estabelece os critérios de aceitação. Gabriel, como Desenvolvedor, implementa as funcionalidades, revisa o código, cria e executa testes e corrige os defeitos encontrados. Dessa forma, a qualidade é construída durante todo o desenvolvimento e não depende exclusivamente de um profissional de QA.

---

## 3. Tarefa 2: Papéis e competências

| Integrante | Papel analisado | Responsabilidades relacionadas à qualidade | Competências técnicas | Competências comportamentais |
|---|---|---|---|---|
| William | Responsável pelo produto — Product Owner | Definir valor e prioridades, validar critérios de aceitação, priorizar defeitos, aceitar ou rejeitar o incremento e decidir sobre a liberação. | Gestão de backlog, critérios de aceitação, priorização por valor e risco, conhecimento do negócio e métricas do produto. | Comunicação, negociação, tomada de decisão, visão sistêmica e equilíbrio entre valor, prazo e risco. |
| Gabriel | Desenvolvedor | Implementar a solução, criar testes unitários e de integração, revisar código, corrigir defeitos e observar requisitos funcionais e não funcionais. | Programação, arquitetura, versionamento, testes automatizados, revisão de código, depuração, integração contínua e segurança. | Responsabilidade, colaboração, pensamento crítico, abertura a feedback e melhoria contínua. |

---

## 4. Tarefa 3: Matriz de responsabilidades

Classificações utilizadas:

- **R:** responsável por executar a atividade;
- **A:** aprovador ou responsável final;
- **C:** consultado antes da execução ou decisão;
- **I:** informado sobre o resultado.

| Atividade de qualidade | Product Owner | Desenvolvedor |
|---|:---:|:---:|
| Definir critérios de aceitação | R/A | C |
| Revisar requisitos | R/A | C |
| Implementar a funcionalidade | I | R/A |
| Revisar o código | I | R/A |
| Criar testes unitários | I | R/A |
| Planejar e executar testes do sistema | C | R/A |
| Registrar e acompanhar defeitos | C | R/A |
| Priorizar a correção dos defeitos | R/A | C |
| Aprovar a disponibilização da versão | A | R |

### 4.1 Lacuna ou conflito encontrado

**Lacuna ou conflito:**  
Considerando os dois papéis selecionados para a análise, as atividades de implementação, revisão do código, criação e execução dos testes e acompanhamento dos defeitos ficam concentradas no Desenvolvedor.

**Consequência:**  
Essa concentração pode sobrecarregar o Desenvolvedor e reduzir a independência da avaliação, pois o mesmo papel implementa, revisa e testa a funcionalidade. Isso aumenta o risco de alguns defeitos não serem identificados. Para reduzir esse problema, o Product Owner deve definir e validar os critérios de aceitação, analisar os resultados apresentados e decidir sobre a liberação. O Desenvolvedor deve registrar os testes e as evidências de maneira clara e, quando possível, solicitar a revisão técnica de outro integrante.

### 4.2 Práticas de QA recomendadas

| Prática recomendada | Problema que ajuda a resolver | Papéis envolvidos |
|---|---|---|
| Definição de Pronto compartilhada e refinamento conjunto dos critérios de aceitação. | Reduz a dúvida sobre quando uma funcionalidade está concluída e ajuda a prevenir entregas incompletas e defeitos. | Product Owner: define e valida os critérios de aceitação; Desenvolvedor: analisa a viabilidade técnica, implementa e verifica o atendimento aos critérios. |
| Registro centralizado de defeitos com prioridade, responsável, prazo, estado e revisão periódica. | Evita que problemas sejam esquecidos, melhora o acompanhamento das correções e torna a decisão de liberação rastreável. | Desenvolvedor: registra, acompanha e corrige os defeitos; Product Owner: define as prioridades e decide sobre a liberação com base nos resultados apresentados. |

---

## 5. Uso de inteligência artificial

**Ferramenta utilizada:**  
ChatGPT, da OpenAI.

**Como foi utilizada:**  
A ferramenta apoiou a estruturação do diagnóstico, a revisão das competências, a distribuição dos papéis entre a dupla e a conferência da matriz RACI.

**Como as respostas foram verificadas:**  
Nós conferimos juntos as regras da matriz RACI, verificando se cada atividade possui pelo menos um Responsável e somente um Aprovador. Também revisamos se as responsabilidades descrevem claramente o que cada papel deve fazer e se as competências representam os conhecimentos, as habilidades e os comportamentos necessários para desempenhar cada papel.
