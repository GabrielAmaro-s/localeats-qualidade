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

Não. William, nos papéis de Product Owner e Analista, esclarece necessidades, prioridades e critérios de aceitação. Gabriel, nos papéis de Desenvolvedor e QA, previne defeitos durante a implementação e produz evidências por meio dos testes. O QA coordena avaliações e comunica riscos, mas a qualidade continua sendo responsabilidade de toda a equipe.

---

## 3. Tarefa 2: Papéis e competências

| Integrante | Papel analisado | Responsabilidades relacionadas à qualidade | Competências técnicas | Competências comportamentais |
|---|---|---|---|---|
| William | Responsável pelo produto — Product Owner | Definir valor e prioridades, validar critérios de aceitação, priorizar defeitos, aceitar ou rejeitar o incremento e decidir sobre a liberação. | Gestão de backlog, critérios de aceitação, priorização por valor e risco, conhecimento do negócio e métricas do produto. | Comunicação, negociação, tomada de decisão, visão sistêmica e equilíbrio entre valor, prazo e risco. |
| William | Analista de sistemas ou de negócio | Elicitar e revisar requisitos, detalhar regras e cenários, remover ambiguidades, manter a rastreabilidade e apoiar a validação. | Modelagem de processos e requisitos, elicitação, análise de regras de negócio, critérios de aceitação e rastreabilidade. | Escuta ativa, pensamento analítico, clareza na comunicação, colaboração e atenção aos detalhes. |
| Gabriel | Desenvolvedor | Implementar a solução, criar testes unitários e de integração, revisar código, corrigir defeitos e observar requisitos funcionais e não funcionais. | Programação, arquitetura, versionamento, testes automatizados, revisão de código, depuração, integração contínua e segurança. | Responsabilidade, colaboração, pensamento crítico, abertura a feedback e melhoria contínua. |
| Gabriel | QA ou analista de qualidade | Analisar riscos, planejar testes, preparar dados e cenários, registrar evidências e defeitos, acompanhar correções e comunicar a situação da qualidade. | Técnicas de teste, testes exploratórios e automatizados, gestão de defeitos, análise de risco e documentação de evidências. | Curiosidade, comunicação objetiva, organização, imparcialidade, colaboração e postura investigativa. |

---

## 4. Tarefa 3: Matriz de responsabilidades

Classificações utilizadas:

- **R:** responsável por executar a atividade;
- **A:** aprovador ou responsável final;
- **C:** consultado antes da execução ou decisão;
- **I:** informado sobre o resultado.

| Atividade de qualidade | Product Owner | Analista | Desenvolvedor | QA |
|---|:---:|:---:|:---:|:---:|
| Definir critérios de aceitação | A | R | C | C |
| Revisar requisitos | C | R/A | C | C |
| Implementar a funcionalidade | I | C | R/A | I |
| Revisar o código | I | I | R/A | C |
| Criar testes unitários | I | I | R/A | C |
| Planejar e executar testes do sistema | I | C | C | R/A |
| Registrar e acompanhar defeitos | C | I | C | R/A |
| Priorizar a correção dos defeitos | R/A | C | C | C |
| Aprovar a disponibilização da versão | A | I | R | C |

### 4.1 Lacuna ou conflito encontrado

**Lacuna ou conflito:**  
A aprovação da disponibilização poderia gerar conflito entre William, como Product Owner, e Gabriel, como QA, caso os dois fossem tratados como aprovadores finais da versão.

**Consequência:**  
A existência de dois aprovadores poderia gerar decisões contraditórias, atrasar a liberação e deixar incerto quem responde pelo resultado. Na matriz, o Product Owner é o único aprovador, o Desenvolvedor executa a disponibilização e o QA é consultado para apresentar evidências e riscos. Assim, o parecer de qualidade informa a decisão sem criar dois aprovadores.

### 4.2 Práticas de QA recomendadas

| Prática recomendada | Problema que ajuda a resolver | Papéis envolvidos |
|---|---|---|
| Definição de Pronto compartilhada e refinamento conjunto dos critérios de aceitação. | Reduz a dúvida sobre quando uma funcionalidade está concluída e distribui a prevenção de defeitos entre os papéis. | William e Gabriel, atuando nos quatro papéis analisados. |
| Registro centralizado de defeitos com prioridade, responsável, prazo, estado e triagem periódica. | Evita que problemas sejam esquecidos, melhora o acompanhamento e torna a decisão de liberação rastreável. | Gabriel registra e acompanha; William prioriza e decide com base nas evidências. |

---

## 5. Uso de inteligência artificial

**Ferramenta utilizada:**  
ChatGPT, da OpenAI.

**Como foi utilizada:**  
A ferramenta apoiou a estruturação do diagnóstico, a revisão das competências, a distribuição dos papéis entre a dupla e a conferência da matriz RACI.

**Como as respostas foram verificadas:**  
A dupla conferiu as regras da matriz RACI: cada atividade possui pelo menos um Responsável e somente um Aprovador. Também revisou se responsabilidade descreve o que o papel faz e se competência descreve o que a pessoa precisa saber ou demonstrar.
