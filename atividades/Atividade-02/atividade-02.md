# Atividade 2: Organização da Qualidade no LocalEats

> Substituam os campos entre colchetes pelas respostas da equipe e removam as instruções antes da entrega.

## 1. Identificação

**Turma:** Noite  
**Equipe:** Luis Matheus dos Santos 


### Integrantes

| Nome | Usuário no GitHub |
|---|---|
|  Luis Matheus dos Santos | luiszr21 |

**Elemento de Competência:** Identificar papéis, responsabilidades e competências relacionadas às atividades de qualidade e testes.

---

## 2. Tarefa 1: Diagnóstico da situação

### 2.1 Problemas organizacionais

| Problema identificado | Possível consequência para o produto ou para a equipe |
|---|---|
| Falta de critérios claros para saber quando uma tarefa está pronta  | Entrega de sistemas com erros, cliente insatisfeito e retrabalho constante |
| Deixar a responsabilidade dos testes apenas para o QA | O QA fica sobrecarregado, vira um gargalo e os devs deixam de testar o próprio código |
| Falta de processo para registrar bugs e aprovar novos lançamentos | Ninguém sabe quem autorizou subir o sistema e bugs acabam esquecidos |

### 2.2 Responsabilidade pela qualidade

**A qualidade do LocalEats deve ser responsabilidade exclusiva do profissional de QA? Justifiquem.**

Não. A qualidade deve ser de todo o time, o Product Owner garante requisitos claros, o Desenvolvedor escreve um código limpo e testado, e o QA atua como estrategista e facilitador dos testes. Deixar os testes só com o QA atrasa as entregas e gera muito retrabalho.

---

## 3. Tarefa 2: Papéis e competências

> Cada integrante deve ser responsável pela análise de pelo menos um papel. Acrescentem ou removam linhas conforme a composição da equipe e os papéis escolhidos.

| Integrante | Papel analisado | Responsabilidades relacionadas à qualidade | Competências técnicas | Competências comportamentais |
|---|---|---|---|---|
| Luis Matheus | Analista de Qualidade (QA) | Criar e rodar testes do sistema, ajudar a definir critérios de aceitação e registrar bugs | Testes manuais e automatizados e lógica de testes | Atenção aos detalhes, boa comunicação e pensamento crítico|

---

## 4. Tarefa 3: Matriz de responsabilidades

> Substituam “Papel 1”, “Papel 2”, “Papel 3” e “Papel 4” pelos papéis definidos pela equipe. Acrescentem ou removam colunas conforme necessário.

Utilizem:

- **R:** responsável por executar a atividade;
- **A:** aprovador ou responsável final;
- **C:** consultado antes da execução ou decisão;
- **I:** informado sobre o resultado.

| Atividade de qualidade | QA | 
|---|:---:|:---:|:---:|:---:|
| Definir critérios de aceitação |  |  |  |  |
| Definir critérios de aceitação | **C** |
| Revisar requisitos | **C** |
| Implementar a funcionalidade | **I** |
| Revisar o código | **I** |
| Criar testes unitários | **C** |
| Planejar e executar testes do sistema | **A / R** |
| Registrar e acompanhar defeitos | **A / R** |
| Priorizar a correção dos defeitos | **C** |
| Aprovar a disponibilização da versão | **C** |
### 4.1 Lacuna ou conflito encontrado

**Lacuna ou conflito:**  
Conflito de responsabilidade na aprovação da versão para produção, onde o QA apenas consulta  mas não tem poder de veto se o sistema estiver com bugs graves

**Consequência:**  
O app pode ser lançado com falhas para os clientes por pressão de prazo, gerando reclamações, prejuízo e perda de usuários

### 4.2 Práticas de QA recomendadas

| Prática recomendada | Problema que ajuda a resolver | Papéis envolvidos |
|---|---|---|
| Critérios de Aceitação Claros | Evita que funcionalidades sejam enviadas para teste sem regras definidas, reduzindo o envio de bugs| QA, Dev e PO |
| desde o início | Envolve o QA no planejamento das tarefas para pegar erros de lógica em requisitos antes do código ser escrito, barateando a correção | QA e PO |

---

## 5. Uso de inteligência artificial

**Ferramenta utilizada:**  
Gemini
**Como foi utilizada:**  
Ajuda na organização das ideias e elaboração do que faz parte do papel de um QA
**Como as respostas foram verificadas:**  
Lido e conferido passo a passo por mim