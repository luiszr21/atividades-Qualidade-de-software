# Atividade 3: Estratégia e Projeto de Testes do LocalEats

## 1. Identificação

**Turma:** Qualidade de Software
**Equipe:** Trabalho Individual
**Data:** 22/09/2026

### Integrantes

| Nome | Usuário no GitHub |
|---|---|
| Luis Matheus | @luiszr21 |

**Elemento de Competência:** Planejar e projetar testes selecionando técnicas adequadas.

**Aplicação:** <https://local-eats-unisenac.vercel.app/>

---

## 2. Tarefa 1: Planejamento dos testes

### 2.1 Objetivo dos testes

Verificar se, após o cliente realizar um pedido na plataforma, este é exibido corretamente na tela de consulta de pedidos contendo todas as informações necessárias (itens, valor e status), garantindo também o tratamento para contas sem compras e o bloqueio/redirecionamento caso não exista sessão ativa no sistema.

### 2.2 Escopo

#### Funcionalidades incluídas

| Integrante | Funcionalidade incluída | O que será verificado |
|---|---|---|
| Luis Matheus | Consultar pedidos | Exibição correta dos dados do pedido recém-realizado, mensagem de lista vazia e bloqueio de acesso ao site/tela sem autenticação. |

#### Funcionalidade não incluída

| Funcionalidade não incluída | Justificativa |
|---|---|
| Filtrar restaurantes por especialidade | Não faz parte do fluxo de consulta de pedidos definido para o escopo individual. |

### 2.3 Abordagem

| Item | Decisão da equipe | Justificativa |
|---|---|---|
| Níveis de teste | Teste de Sistema | Avaliação do fluxo completo diretamente pela interface web. |
| Tipos de teste | Funcional | Validação das regras de exibição e controle de acesso dos pedidos. |
| Perspectiva caixa-preta ou caixa-branca | Caixa-preta | Validação focada nas entradas do usuário e saídas visíveis na tela, sem análise do código. |
| Técnicas de teste | Tabela de Decisão | Mapeamento das combinações de estado da sessão de login e presença de histórico de compras.|

### 2.4 Ambiente e responsabilidades

| Item | Definição |
|---|---|
| Ambiente necessário | Navegador Web e acesso à URL `https://local-eats-unisenac.vercel.app/static/orders.html` com conta criada. |
| Responsáveis pelo planejamento | Luis Matheus |
| Responsáveis pela especificação dos casos | Luis Matheus |
| Responsáveis pela futura execução | Luis Matheus |

### 2.5 Critérios

| Critério | Definição da equipe |
|---|---|
| Entrada | Aplicação online e conta de usuário criada na plataforma. |
| Saída | Os 3 casos de teste planejados executados e registrados. |
| Suspensão | Indisponibilidade da aplicação ou falha no serviço de autenticação do sistema. |

---

## 3. Tarefa 2: Riscos e técnicas de teste

### 3.1 Análise dos riscos

| ID | Integrante | Funcionalidade | Risco | Consequência | Probabilidade | Impacto | Prioridade | Justificativa |
|---|---|---|---|---|:---:|:---:|:---:|---|
| R01 | Luis Matheus | Consultar pedidos | Tentativa de acesso direto à tela de pedidos sem estar autenticado no sistema | Falha de segurança por permitir navegação anônima ou comportamento inconsistente da aplicação | Média | Alto | Alta | Como o sistema exige login para acesso, permitir a visualização anônima compromete a privacidade dos dados. |
| R02 | Luis Matheus | Consultar pedidos | O pedido recém-realizado não aparecer no histórico ou omitir informações essenciais | O cliente fica sem confirmação dos detalhes da compra e status da entrega | Média | Médio | Média | Impede que o cliente verifique os itens e o valor do pedido que acabou de fazer. |

### 3.2 Aplicação das técnicas

#### Análise do integrante 1

**Integrante:** Luis Matheus  
**Funcionalidade:** Consultar pedidos  
**Risco relacionado:** R01 e R02  
**Técnica escolhida:** Tabela de decisão

**Por que a técnica foi escolhida:**  
A Tabela de Decisão foi escolhida porque a exibição da tela depende de decisões combinadas de autenticação e estado da conta: o sistema bloqueia qualquer acesso sem login ativo e, para usuários autenticados, decide entre exibir os detalhes do pedido recém-realizado ou a mensagem de ausência de compras.[cite: 1, 2]

**Aplicação da técnica:**  

| Usuário Autenticado? | Realizou Pedido? | Comportamento do Sistema |
|:---:|:---:|---|
| **Sim** | **Sim** | Carrega a tela e exibe o pedido recém-realizado com todos os detalhes (itens, valor e status). |
| **Sim** | **Não** | Carrega a tela e exibe mensagem informando que não existem pedidos cadastrados. |
| **Não** | **Não se aplica** | Bloqueia o acesso ao site/tela e redireciona imediatamente para a página de login/cadastro. |

**Casos derivados:** CT01, CT02 e CT03

---

## 4. Tarefa 3: Casos de teste e rastreabilidade

### 4.1 Casos de teste

### CT01: Exibir informações completas do pedido recém-realizado

**Integrante responsável:** Luis Matheus  
**Funcionalidade:** Consultar pedidos  
**Risco ou requisito relacionado:** R02  
**Técnica utilizada:** Tabela de decisão

**Pré-condição:**  
Usuário cadastrado, autenticado na aplicação e em processo de finalização de uma compra.

**Dados de entrada:**  
Não se aplica.

**Passos:**

1. Acessar o LocalEats com a conta criada.
2. Selecionar um restaurante, adicionar itens ao carrinho e concluir o pedido.
3. Navegar para a tela de consulta de pedidos (`/static/orders.html`).

**Resultado esperado:**  
O pedido recém-efetuado é listado com sucesso, apresentando todas as informações necessárias (itens selecionados, valor total e status do pedido).

---

### CT02: Consultar pedidos com usuário autenticado sem compras realizadas

**Integrante responsável:** Luis Matheus  
**Funcionalidade:** Consultar pedidos  
**Risco ou requisito relacionado:** R02  
**Técnica utilizada:** Tabela de decisão

**Pré-condição:**  
Usuário recém-cadastrado e autenticado no sistema, sem nenhum pedido efetuado.

**Dados de entrada:**  
Não se aplica.

**Passos:**

1. Criar uma nova conta no LocalEats.
2. Acessar a tela de consulta de pedidos (`/static/orders.html`).

**Resultado esperado:**  
A tela carrega informando que não existem pedidos cadastrados para a conta.

---

### CT03: Tentar acessar a tela de pedidos sem estar autenticado

**Integrante responsável:** Luis Matheus  
**Funcionalidade:** Consultar pedidos  
**Risco ou requisito relacionado:** R01  
**Técnica utilizada:** Tabela de decisão

**Pré-condição:**  
Navegador sem sessão iniciada/autenticada no LocalEats.

**Dados de entrada:**  
URL: `https://local-eats-unisenac.vercel.app/static/orders.html`

**Passos:**

1. Abrir uma aba anônima no navegador.
2. Tentar acessar diretamente o link da tela de pedidos.

**Resultado esperado:**  
O acesso à página é bloqueado e o sistema redireciona automaticamente o usuário para a tela de login/cadastro.

---

### 4.2 Matriz de rastreabilidade

| Integrante | Funcionalidade | Risco ou requisito | Técnica utilizada | Casos de teste |
|---|---|---|---|---|
| Luis Matheus | Consultar pedidos | R01 | Tabela de decisão | CT03 |
| Luis Matheus | Consultar pedidos | R02 | Tabela de decisão | CT01, CT02 |

---

## 5. Uso de inteligência artificial

**Ferramenta utilizada:**  
Gemini (Google AI)

**Como foi utilizada:**  
Foi usado para validar ideias e como consulta para perguntas e duvidas relacionadas a testes.

**Uma sugestão que precisou ser alterada ou rejeitada:**  
A sugestão inicial assumia que a tela de pedidos poderia ser aberta por usuários anônimos e exibir dados vazios, sendo corrigida para refletir a obrigatoriedade de login para navegação no site.

**Como as respostas foram verificadas:**  
Revisão manual comparando os passos dos testes com a documentação do trabalho e o comportamento real da aplicação LocalEats.
