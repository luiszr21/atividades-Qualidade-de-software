# Atividade 1: Fundamentos e Características da Qualidade no LocalEats

> Substituam os campos entre colchetes pelas respostas da equipe e removam as instruções antes da entrega.

## 1. Identificação

**Turma:** Noite 
**Equipe:** Luis Matheus dos Santos  


### Integrantes

| Nome | Usuário no GitHub |
|---|---|
| Luis Matheus dos Santos  | luiszr21 |

**Elemento de Competência:** Compreender os fundamentos de qualidade de software e sua aplicação no desenvolvimento de sistemas.

**Aplicação:** <https://local-eats-unisenac.vercel.app/>

---

## 2. Tarefa 1: Fundamentos da qualidade

### 2.1 Necessidades explícitas e implícitas

| Tipo | Necessidade | Interessado | Consequência se não for atendida |
|---|---|---|---|
| Explícita | Filtrar restaurantes por especialidade. | Cliente | Dificuldade em encontrar pratos do interesse, levando ao abandono do aplicativo. |
| Explícita | Criar conta | Cliente e LocalEats | Impossibilidade de rastrear pedidos por usuário e personalizar a experiência de uso |
| Implícita | Garantir a segurança | Cliente e LocalEats | Vazamento de informações sensíveis |
| Implícita | Rastreio de entrega | Cliente | Cliente fica ansioso por não saber quando pedido vai chegar |

### 2.2 Questão sobre os fundamentos da qualidade

**Um sistema que implementa todas as funcionalidades explicitamente solicitadas pode, ainda assim, apresentar baixa qualidade? Justifiquem utilizando pelo menos uma necessidade implícita identificada pela equipe.**

Sim. Um sistema pode ter todas as funcionalidades previstas e apresentar baixa qualidade se não atender às necessidades dos usuários. Por exemplo, o LocalEats pode permitir fazer pedidos, mas, se não garantir a segurança dos dados de pagamento ou não compartilhar a localização da entrega, o usuário perderá a confiança na plataforma.

---

## 3. Tarefa 2: Exploração da aplicação

> Cada integrante deve explorar uma funcionalidade, realizando uma utilização esperada e uma utilização alternativa, inválida ou incompleta. Acrescentem ou removam linhas conforme o número de integrantes.

| Integrante | Funcionalidade | O que foi realizado | O que foi observado | Evidência |
|---|---|---|---|---|
| Luis Matheus | Filtrar restaurantes por especialidade | Clicou para filtrar a eespecialidade para Japonesa. Uso alternativo: desmarcar o filtro para ver se o sistema volta a exibir "Todos" | O sistema aplicou o filtro corretamente | [ver evidência](evidencias/luis-filtrar-especialidade.png) |




---

## 4. Tarefa 3: Requisitos e características de qualidade

> Cada integrante deve formular um requisito de qualidade relacionado à mesma funcionalidade explorada na Tarefa 2. Acrescentem ou removam linhas conforme o número de integrantes.

| Integrante | Requisito de Qualidade | Característica ou subcaracterística | Justificativa | Como avaliar |
|---|---|---|---|---|
| Luis Matheus | O sistema deve filtrar e atualizar a lista de restaurantes em menos de 1 segundo ao selecionar uma especialidade. | Eficiência de Desempenho / Comportamento no tempo | Evita a lentidão e garante uma navegação fluida ao buscar refeições no LocalEats. | Cronometrar o tempo entre o clique no filtro e a atualização da tela usando a aba Network do navegador (F12). |

---

## 5. Uso de inteligência artificial

**Ferramenta utilizada:**  
Gemini
**Como foi utilizada:**  
Auxiliou na compreensão da ISO/IEC 25010, nos requisitos de qualidade

**Como as respostas foram verificadas:**  
 As respostas foram revisadas e comparadas com os testes realizados no LocalEats