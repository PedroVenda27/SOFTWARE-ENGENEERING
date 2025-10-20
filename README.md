Este repositório contém todo o Conteudo Dado Nas Aulas bem como o Projeto Final da unidade curricular De Engenharia de Software do curso de Informática (2.º ano, UMAIA).

Para esta Cadeira Como Projeto Final foi Pedido o desenvolvimento de uma ideia de um projeto App OU API e desenvolvendo toda a estrutura e engenharia que esta implicaria

---
---

# Relatório de desenvolvimento TASKLY_APP


Aqui vai encontrar encontrar todo o relatorio de Desenvolvimento da TASKLY_APP desenvolvido por
Carolina Fernandes (A044897) Bernardo Macedo (A042429) Pedro Venda (A045464) Ruben Garcia (A047635)


## Visão de Produto - Taskly

### 1. Introdução

A nossa aplicação de gestão de tarefas e produtividade tem como objetivo oferecer uma solução intuitiva, eficiente e colaborativa para usuários individuais e equipes organizarem o seu dia a dia.

Esta terá como funcionalidades de criação de tarefas, pastas, etiquetas, calendário, notificações e integração com Google Calendar, a aplicação facilitará a organização do dia a dia, aumentando a produtividade do utilizador.

Este produto será uma ferramenta indispensável para quem busca melhorar a organização e a produtividade, seja individualmente ou em equipa. 
Combinando funcionalidades poderosas e uma experiência intuitiva, a aplicação permitirá que usuários gerenciem suas tarefas de forma eficiente e sem complicações.

Slogan: "TASKLY Organize. Priorize. Conclua. Produtividade sem complicação!!"

### 2. Funcionalidades Principais
 - Criação de Tarefas 
 - Criação de Pastas e Etiquetas
 - Calendário
 - Notificação/Alertas de Entregas Tarefas
 - WhiteBoard
 - Integração/ Sincronização com Google Calendar


### 3. Suposições e Dependências
 - Integração / Sincronização com Google Calendar
   
---

## Requirements

1.1 Requisitos Funcionais

 - Permitir a criação, edição e exclusão de tarefas.
 - Permitir a criação, edição e exclusão de pastas para organização de tarefas.
 - Possibilitar a adição de etiquetas para categorização das tarefas.
 - Oferecer um calendário integrado para visualização de prazos e agendamentos.
 - Permitir integração e sincronização com o Google Calendar.
 - Enviar notificações e alertas sobre prazos de tarefas.
 - Possibilitar a visualização das tarefas em um quadro branco interativo.
 - Permitir pesquisa e filtragem de tarefas por etiquetas, pastas e datas.

1.2 Requisitos Não Funcionais

 - interface intuitiva e responsiva.
 - aplicação via web e dispositivos móveis.
 - tempo de resposta das funcionalidades 
 - Dados Pessoais deve ser armazenados de forma segura e criptografada.

---

## Use Case Model / Use Case Table

Criámos um diagrama de casos de uso em UML para representar graficamente os principais casos de uso da aplicação e os atores envolvidos, clarificando o contexto e os limites do sistema. Além disso, elaborámos uma tabela de casos de uso que descreve, de forma detalhada, cada uma das funcionalidades de alto nível, com os respetivos objetivos, atores e descrições, seguindo uma abordagem orientada a resultados (verbo + substantivo). Esta combinação permite uma visão clara e completa das interações esperadas entre os utilizadores e o sistema.

Este é o nosso [Use Case Model](https://github.com/PedroVenda27/SOFTWARE-ENGENEERING/blob/main/docs/ModeloCasoSUso.md)

Este é o nossa [Use Case Table](https://github.com/PedroVenda27/SOFTWARE-ENGENEERING/blob/main/docs/TabelasCasosdeUso.md)


## User Stories

Uma história de usuário é uma descrição da funcionalidade desejada contada da perspectiva do usuário ou cliente. 
Estas são compostas com base no modelo

*As a < user role >, I want < goal > so that < reason >.*

Estas sao as nossas User Stories [User Stories](https://github.com/UM-UCs-Org/es-2425-tat1/issues). Esta estão todas inseridas na Label "User Stories".

## User Interface Mockups

![Ecra Principal](https://github.com/user-attachments/assets/59371a9f-168e-45ff-8bb3-90e6472cecb6)
![Calendário](https://github.com/user-attachments/assets/040563ea-d088-4167-97f6-2f454a41107e)


## Acceptance Test

Para cada user story, escrevemos também os testes de aceitação de forma textual, utilizando a linguagem Gherkin. Estes testes consistem na descrição de cenários que ajudam a confirmar que o sistema satisfaz os requisitos definidos pela user story, permitindo validar o comportamento esperado de forma clara e compreensível para todos os intervenientes no projeto.

Este são os nossos [Acceptance Tests](https://github.com/PedroVenda27/SOFTWARE-ENGENEERING/blob/main/docs/TestesAceita%C3%A7%C3%A3o.md)


## Product Backloging / Value And Effort
Utilizámos o método MoSCoW para priorizar as user stories, classificando-as em Must have, Should have, Could have e Won’t have, de forma a assegurar que a equipa se concentra primeiro nos requisitos mais críticos para o sucesso do projeto. Além disso, estimámos o esforço necessário para cada user story com base em tamanhos de t-shirt (XS, S, M, L, XL), facilitando o planeamento e a gestão da carga de trabalho.

Este é o nosso Product Backloging [Product Backloging](https://github.com/orgs/UM-UCs-Org/projects/25)

## Domain model

To better understand the context of the software system, it is very useful to have a simple UML class diagram with all the key concepts (names, attributes) and relationships involved of the problem domain addressed by your module. 
Also provide a short textual description of each class. 

 <p align="center" justify="center">
  <img src="https://github.com/UM-UCs-Org/es-2425-tat1/blob/main/images/Diagrama_2.png"/>  
</p>

## Vertical Prototype

![image](https://github.com/user-attachments/assets/4bdb29c1-8dd5-4813-af8d-011c5b9df4ce)

## Use case Model

![image](https://github.com/user-attachments/assets/e2d3447b-40db-4f04-a0d8-d8f80ba311f2)


## Architecture and Design

Relativamente ao desenvolvimento do sistema, a arquitetura foi pensada de forma a facilitar a integração de novos programadores e otimizar a manutenção e evolução do código. O objetivo era garantir que qualquer novo membro da equipa conseguisse compreender rapidamente o funcionamento do sistema e contribuir com modificações ou melhorias sem grandes dificuldades.

Para documentar a arquitetura, optámos por descrever a decomposição do sistema nos seus principais componentes e destacar as interações e colaborações entre eles. Além disso, resolvemos problemas típicos através da aplicação de padrões arquiteturais e de design amplamente conhecidos, o que garantiu um sistema mais robusto e escalável.

Na parte de arquitetura lógica, criámos um diagrama UML que mostra a estrutura de alto nível do sistema, sem nos preocuparmos com a alocação de recursos ou componentes específicos. A decomposição foi feita tanto de forma horizontal quanto vertical:

Decomposição horizontal: Dividimos o sistema em camadas, como a interface do usuário, a lógica de negócios e a camada de dados. Cada camada tem responsabilidades bem definidas, facilitando a manutenção e a implementação de novos recursos.

Decomposição vertical: Criámos uma hierarquia de subsistemas que representam as diferentes partes do sistema, cada uma com sua própria função e que se comunicam entre si de maneira bem estruturada. Isso ajuda a manter a organização do código e facilita a adição de novos módulos sem comprometer as partes já existentes.

Por exemplo, no caso da nossa app de calendário e tarefas, utilizámos essa abordagem para organizar os pacotes e subsistemas de maneira que cada um tivesse uma responsabilidade clara, como interfaces específicas baseadas num modelo e bases de dados específicas, tornando o sistema mais modular e fácil de expandir no futuro.

Essa arquitetura não só torna o código mais fácil de entender, mas também facilita a adição de novos componentes ou funcionalidades, sem impactar negativamente o desempenho ou a estabilidade do sistema.

![image](https://github.com/user-attachments/assets/4d9f3a41-a21d-4887-bffc-945dd5c114ee)


### Physical architecture

O objetivo desta subseção é documentar a estrutura física de alto nível do sistema de software (máquinas, conexões, componentes de software instalados e suas dependências) usando diagramas UML de implantação (Visão de Implantação) ou diagramas de componentes (Visão de Implementação), separados ou integrados, mostrando a estrutura física do sistema.

Para a Taskly, o diagrama UML de implantação irá mostrar a relação entre os componentes e os artefatos necessários para a execução do sistema. Como exemplo de tecnologias relevantes, para o desenvolvimento de apps móveis, escolhemos FlutterFlow como o framework principal. FlutterFlow é uma plataforma de desenvolvimento visual baseada em Flutter, permitindo criar aplicações nativas de alto desempenho para Android e iOS com uma única base de código, de maneira rápida e eficiente. Essa escolha foi feita para otimizar o tempo de desenvolvimento e garantir a consistência entre as plataformas.

Além disso, consideramos tecnologias como Firebase para o backend, dado que oferece uma solução robusta para autenticação, armazenamento de dados em tempo real e outras funcionalidades essenciais para o nosso sistema.

Diagrama de Implantação (Deployment View)

A seguir, apresentamos um diagrama de implantação UML mostrando a visão física do sistema. No lugar de componentes de software, representamos as manifestações físicas/executáveis desses componentes, chamados de artefatos em UML. O diagrama é acompanhado por uma breve descrição de cada nó e artefato.

![image](https://github.com/user-attachments/assets/20ab024c-c081-4399-9cd8-f9f37f6b5508)

---

## Test Guide

### O Utilizador Dever tentar fazer todas estas tarefas de forma a testar a aplicação 

1. O utilizador faz login com "Get Started"
2. O utilizador faz login com o Google
3. O utilizador faz login com o Facebook
4. O utilizador tenta visualizar as tarefas do dia
5. O utilizador tenta verificar quais são as tarefas urgentes (vermelho)
6. O utilizador tenta verificar quais são as tarefas normais (verde)
7. O utilizador tenta criar uma tarefa normal
8. O utilizador tenta criar uma tarefa importante
9. O utilizador seleciona a hora e o dia da tarefa a criar
10. O utilizador tenta visualizar uma tarefa específica
11. O utilizador tenta editar uma tarefa
12. O utilizador tenta visualizar todas as notas
13. O utilizador tenta visualizar as notas da categoria “Class Notes”
14. O utilizador tenta editar uma nota
15. O utilizador começa a editar uma nota, mas arrepende-se e cancela
16. O utilizador tenta criar uma nova pasta para notas
17. O utilizador tenta visualizar o calendário (movimentando-se nele)
18. O utilizador visualiza as suas tarefas no calendário
19. O utilizador tenta sincronizar o calendário com o Google
20. O utilizador tenta dessincronizar o calendário

### Results from the tests

Participantes: 20 alunos do ISMAI
Método: Observação direta/ teste da app + questionário pós-teste
Objetivo: Avaliar as interações mais comuns na app e identificar pontos de fricção

🟢 Funcionamento Perfeito – 18 a 20 utilizadores (≥ 90%)

- O utilizador faz login com "Get Started"
- O utilizador tenta visualizar as tarefas do dia
- O utilizador tenta verificar quais são as tarefas urgentes (vermelho)
- O utilizador tenta verificar quais são as tarefas normais (verde)
- O utilizador seleciona a hora e o dia da tarefa a criar
- O utilizador tenta visualizar uma tarefa específica
- O utilizador tenta visualizar todas as notas
- O utilizador tenta visualizar as notas da categoria “Class Notes”
- O utilizador começa a editar uma nota, mas arrepende-se e cancela
- O utilizador tenta visualizar o calendário (movimentando-se nele)
- O utilizador visualiza as suas tarefas no calendário
- O utilizador tenta dessincronizar o calendário

🟡 Funcionamento Bom – 15 a 17 utilizadores (75% a 89%)

- O utilizador faz login com o Google
- O utilizador faz login com o Facebook
- O utilizador tenta sincronizar o calendário com o Google
    
🟠 Funcionamento a Melhorar – 10 a 14 utilizadores (50% a 74%)

- O utilizador tenta criar uma nova pasta para notas
- O utilizador tenta editar uma nota
- O utilizador tenta editar uma tarefa
- O utilizador tenta criar uma tarefa normal
- O utilizador tenta criar uma tarefa importante

---

## TASK DIVISION
REQUIREMENTS -- Carolina Fernandes (A044897) Bernardo Macedo (A042429) Pedro Venda (A045464) Ruben Garcia (A047635)
PRODUCT VISION -- Carolina Fernandes (A044897) Bernardo Macedo (A042429) Pedro Venda (A045464) Ruben Garcia (A047635)
USE CASES -- Pedro Venda (A045464) Bernardo Macedo (A042429)
USE STORIES -- Pedro Venda (A045464) Carolina Fernandes (A044897)
UI MOCKUPS -- Pedro Venda (A045464)
ACEPTANCE TEST -- Pedro Venda (A045464) Ruben Garcia (A047635)
DOMAIN MODEL -- Ruben Garcia (A047635)
PRODUCT BACKLOG AND VALUE EFFORT -- Pedro Venda (A045464)
VERTICAL PROTOTYPE -- Pedro Venda (A045464)
PRODUCT INCREMENT #0 -- Pedro Venda (A045464)
BOARD IS WELL USED #0 -- Pedro Venda (A045464)
PRODUCT INCREMENT #1 -- Pedro Venda (A045464)
BOARD IS WELL USED #1 -- Pedro Venda (A045464) Carolina Fernandes (A044897) Ruben Garcia (A047635)
PRODUCT INCREMENT #2 -- Pedro Venda (A045464) Carolina Fernandes (A044897) Ruben Garcia (A047635)
BOARD IS WELL USED #2 -- Pedro Venda (A045464) Carolina Fernandes (A044897)
LOGICAL UML DIAGRAM -- Pedro Venda (A045464)
PHYSICAL UML DIAGRAM -- Pedro Venda (A045464)
GITHUB FLOW FLOWED -- Carolina Fernandes (A044897) 22% ; Pedro Venda (A045464) 56% ; Ruben Garcia (A047635) 22%
FLUTTERFLOW -- Carolina Fernandes (A044897) 30% Pedro Venda (A045464) 40% Ruben Garcia (A047635) 30%

GERAL -- Carolina Fernandes (A044897) 28% Pedro Venda (A045464) 44% Ruben Garcia (A047635) 28%
