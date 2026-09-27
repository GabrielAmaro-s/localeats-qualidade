# Atividade 3: Estratégia e Projeto de Testes do LocalEats

## 1. Identificação

**Turma:** 2026/2  
**Equipe:** Gabriel e William  



**Elemento de Competência:** Planejar e projetar testes selecionando técnicas adequadas.

**Aplicação:** <https://local-eats-unisenac.vercel.app/>

---

## 2. Tarefa 1: Planejamento dos testes

### 2.1 Objetivo dos testes

Verificar se o LocalEats controla corretamente o acesso por e-mail e senha e se o cadastro aplica a regra de tamanho mínimo da senha, sem aceitar dados inválidos nem rejeitar dados válidos. Os testes também observarão se as mensagens apresentadas permitem ao usuário compreender o resultado da ação realizada.

### 2.2 Escopo

#### Funcionalidades incluídas

| Integrante | Funcionalidade incluída | O que será verificado |
|---|---|---|
| Gabriel | Entrar no sistema | Acesso com credenciais válidas, bloqueio de credenciais inválidas e validação dos campos obrigatórios. |
| William | Criar conta | Aplicação do mínimo de três caracteres para a senha e comportamento nos valores próximos ao limite. |

#### Funcionalidade não incluída

| Funcionalidade não incluída | Justificativa |
|---|---|
| Fazer pedido | O plano concentra o esforço nos fluxos de identificação que antecedem o uso de favoritos e pedidos. O fluxo de pedidos deverá ser planejado em outro ciclo de testes. |

### 2.3 Abordagem

| Item | Decisão da equipe | Justificativa |
|---|---|---|
| Níveis de teste | Teste de sistema | Os fluxos serão avaliados pela interface completa, considerando as respostas observáveis do LocalEats. |
| Tipos de teste | Teste funcional com observações de usabilidade | O foco principal são as regras de autenticação e cadastro. A clareza das mensagens será observada como apoio à correção do usuário. |
| Perspectiva caixa-preta ou caixa-branca | Caixa-preta | Os casos utilizam entradas e resultados esperados sem depender do conhecimento do código-fonte. |
| Técnicas de teste | Tabela de decisão e análise de valor limite | O login depende de combinações de condições, enquanto a senha possui uma fronteira explícita em três caracteres. |

### 2.4 Ambiente e responsabilidades

| Item | Definição |
|---|---|
| Ambiente necessário | Aplicação disponível; navegador Chrome ou Firefox atualizado; computador com conexão estável; contas e e-mails fictícios; uma conta previamente cadastrada para os testes de login. |
| Responsáveis pelo planejamento | Gabriel e William definem conjuntamente objetivo, escopo, abordagem, critérios e prioridades. |
| Responsáveis pela especificação dos casos | Gabriel especifica CT01 a CT03. William especifica CT04 a CT06. Cada integrante revisa os casos do colega. |
| Responsáveis pela futura execução | Gabriel executará CT01 a CT03. William executará CT04 a CT06. As evidências e os defeitos serão revisados pela dupla. |

### 2.5 Critérios

| Critério | Definição da equipe |
|---|---|
| Entrada | Aplicação disponível; navegador e conexão funcionais; conta de teste cadastrada; e-mails fictícios únicos; regra mínima da senha confirmada na interface. |
| Saída | Os seis casos planejados foram executados e registrados; os resultados e as evidências estão completos; qualquer falha encontrada possui descrição, prioridade e responsável. |
| Suspensão | Aplicação ou serviço de autenticação indisponível; cadastro ou login bloqueado por falha externa; ausência dos dados de teste necessários. |

---

## 3. Tarefa 2: Riscos e técnicas de teste

### 3.1 Análise dos riscos

| ID | Integrante | Funcionalidade | Risco | Consequência | Probabilidade | Impacto | Prioridade | Justificativa |
|---|---|---|---|---|:---:|:---:|:---:|---|
| R01 | Gabriel | Entrar no sistema | O sistema permitir uma credencial inválida ou bloquear uma credencial válida. | Acesso indevido ou impedimento do acesso legítimo à conta. | Média | Alto | Alta | O login protege os dados e libera recursos vinculados ao usuário. |
| R02 | William | Criar conta | O limite mínimo da senha ser aplicado de forma incorreta. | Uma senha abaixo do mínimo pode ser aceita ou uma senha válida pode ser rejeitada, prejudicando a segurança e o cadastro. | Média | Médio | Média | A interface declara um mínimo de três caracteres e erros na fronteira são comuns. |

### 3.2 Aplicação das técnicas

#### Análise de Gabriel

**Integrante:** Gabriel  
**Funcionalidade:** Entrar no sistema  
**Risco relacionado:** R01  
**Técnica escolhida:** Tabela de decisão

**Por que a técnica foi escolhida:**  
O resultado do login depende da combinação entre o preenchimento dos campos e a validade das credenciais. A tabela torna cada combinação explícita e reduz a possibilidade de esquecer um comportamento importante.

**Aplicação da técnica:**

| Regra | Campos completos | Credenciais válidas | Resultado esperado | Caso derivado |
|:---:|:---:|:---:|---|:---:|
| 1 | Sim | Sim | Autenticar o usuário e abrir a área protegida. | CT01 |
| 2 | Sim | Não | Negar o acesso e apresentar uma mensagem genérica de credencial inválida. | CT02 |
| 3 | Não | Não se aplica | Impedir o envio e indicar os campos obrigatórios. | CT03 |

**Casos derivados:** CT01, CT02 e CT03.

#### Análise de William

**Integrante:** William  
**Funcionalidade:** Criar conta  
**Risco relacionado:** R02  
**Técnica escolhida:** Análise de valor limite

**Por que a técnica foi escolhida:**  
O campo informa uma senha mínima de três caracteres. Os valores imediatamente abaixo, no limite e imediatamente acima verificam a fronteira entre as classes inválida e válida.

**Aplicação da técnica:**

| Comprimento da senha | Relação com o limite | Classe | Resultado esperado | Caso derivado |
|:---:|---|:---:|---|:---:|
| 2 caracteres | Um abaixo | Inválida | Rejeitar o cadastro e informar o mínimo exigido. | CT04 |
| 3 caracteres | No limite | Válida | Aceitar o cadastro quando os demais dados forem válidos. | CT05 |
| 4 caracteres | Um acima | Válida | Aceitar o cadastro quando os demais dados forem válidos. | CT06 |

**Casos derivados:** CT04, CT05 e CT06.

---

## 4. Tarefa 3: Casos de teste e rastreabilidade

### 4.1 Casos de teste

Os casos abaixo são especificações para execução futura. Nesta atividade, nenhum resultado obtido está sendo registrado.

### CT01: Permitir login com credenciais válidas

**Integrante responsável:** Gabriel  
**Funcionalidade:** Entrar no sistema  
**Risco ou requisito relacionado:** R01  
**Técnica utilizada:** Tabela de decisão — regra 1

**Pré-condição:**  
Existe uma conta de teste ativa e a tela de login está aberta.

**Dados de entrada:**  
E-mail cadastrado e senha correta da conta de teste.

**Passos:**

1. Preencher o e-mail cadastrado.
2. Preencher a senha correta.
3. Selecionar **Entrar**.

**Resultado esperado:**  
O sistema autentica o usuário e exibe a área protegida, sem apresentar mensagem de erro.

---

### CT02: Bloquear login com senha incorreta

**Integrante responsável:** Gabriel  
**Funcionalidade:** Entrar no sistema  
**Risco ou requisito relacionado:** R01  
**Técnica utilizada:** Tabela de decisão — regra 2

**Pré-condição:**  
Existe uma conta de teste ativa e a tela de login está aberta.

**Dados de entrada:**  
E-mail cadastrado e senha incorreta fictícia.

**Passos:**

1. Preencher o e-mail cadastrado.
2. Preencher a senha incorreta.
3. Selecionar **Entrar**.

**Resultado esperado:**  
O sistema não autentica o usuário, mantém o acesso à área protegida bloqueado e apresenta uma mensagem que não revela qual credencial está incorreta.

---

### CT03: Impedir login com campos vazios

**Integrante responsável:** Gabriel  
**Funcionalidade:** Entrar no sistema  
**Risco ou requisito relacionado:** R01  
**Técnica utilizada:** Tabela de decisão — regra 3

**Pré-condição:**  
A tela de login está aberta.

**Dados de entrada:**  
E-mail vazio e senha vazia.

**Passos:**

1. Manter os campos de e-mail e senha vazios.
2. Selecionar **Entrar**.

**Resultado esperado:**  
O sistema impede o envio, mantém a tela de login e indica os campos obrigatórios de forma clara.

---

### CT04: Rejeitar senha com dois caracteres

**Integrante responsável:** William  
**Funcionalidade:** Criar conta  
**Risco ou requisito relacionado:** R02  
**Técnica utilizada:** Análise de valor limite — um abaixo

**Pré-condição:**  
A tela **Criar Conta** está aberta e existe um e-mail fictício ainda não cadastrado.

**Dados de entrada:**  
Nome válido; e-mail fictício único; senha `a1`, com dois caracteres.

**Passos:**

1. Preencher nome e e-mail válidos.
2. Preencher a senha com dois caracteres.
3. Selecionar **Registrar**.

**Resultado esperado:**  
O sistema não cria a conta e informa que a senha deve possuir pelo menos três caracteres.

---

### CT05: Aceitar senha com três caracteres

**Integrante responsável:** William  
**Funcionalidade:** Criar conta  
**Risco ou requisito relacionado:** R02  
**Técnica utilizada:** Análise de valor limite — no limite

**Pré-condição:**  
A tela **Criar Conta** está aberta e existe um e-mail fictício ainda não cadastrado.

**Dados de entrada:**  
Nome válido; e-mail fictício único; senha `a1B`, com três caracteres.

**Passos:**

1. Preencher nome e e-mail válidos.
2. Preencher a senha com três caracteres.
3. Selecionar **Registrar**.

**Resultado esperado:**  
O sistema cria a conta e confirma o cadastro ou direciona o usuário para o próximo passo previsto.

---

### CT06: Aceitar senha com quatro caracteres

**Integrante responsável:** William  
**Funcionalidade:** Criar conta  
**Risco ou requisito relacionado:** R02  
**Técnica utilizada:** Análise de valor limite — um acima

**Pré-condição:**  
A tela **Criar Conta** está aberta e existe outro e-mail fictício ainda não cadastrado.

**Dados de entrada:**  
Nome válido; e-mail fictício único; senha `a1B2`, com quatro caracteres.

**Passos:**

1. Preencher nome e e-mail válidos.
2. Preencher a senha com quatro caracteres.
3. Selecionar **Registrar**.

**Resultado esperado:**  
O sistema cria a conta e confirma o cadastro ou direciona o usuário para o próximo passo previsto.

### 4.2 Matriz de rastreabilidade

| Integrante | Funcionalidade | Risco ou requisito | Técnica utilizada | Casos de teste |
|---|---|---|---|---|
| Gabriel | Entrar no sistema | R01 — autenticação incorreta | Tabela de decisão | CT01, CT02 e CT03 |
| William | Criar conta | R02 — limite mínimo da senha | Análise de valor limite | CT04, CT05 e CT06 |

A matriz confirma que cada risco possui uma técnica e casos de teste associados. Não há risco identificado sem cobertura planejada.

---

## 5. Uso de inteligência artificial

**Ferramenta utilizada:**  
ChatGPT, da OpenAI.

**Como foi utilizada:**  
A ferramenta apoiou a comparação entre técnicas, a redação dos riscos, a organização dos casos e a conferência da rastreabilidade.

**Uma sugestão que precisou ser alterada ou rejeitada:**  
A primeira sugestão utilizava particionamento de equivalência nos dois fluxos. A dupla manteve a tabela de decisão para Gabriel e alterou a técnica de William para análise de valor limite, pois a senha possui uma fronteira explícita em três caracteres e a atividade exige pelo menos duas técnicas diferentes.

**Como as respostas foram verificadas:**  
A dupla comparou o plano com o enunciado, confirmou a indicação de mínimo de três caracteres na interface e conferiu se objetivo, escopo, riscos, técnicas, casos e matriz utilizam os mesmos identificadores.
