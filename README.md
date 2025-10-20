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

## Tabelas Casos De Uso


### Example: Criar Tarefa
|||
| --- | --- |
| *Name* | Criar Tarefa |
| *Actor* | Utilizador | 
| *Description* |- O utilizador cria uma nova tarefa no sistema, podendo atribuir etiquetas, pastas e associá-la ao calendário. |
| *Preconditions* | - O utilizador deve estar autenticado no sistema. <br> - O utilizador deve ter permissão para criar tarefas. |
| *Postconditions* | - Se atribuída ao calendário, a tarefa aparece na agenda. <br> - Se tiver etiquetas ou pastas, a tarefa fica associada a elas. |
| *Normal flow* | 1. O utilizador acede ao sistema. <br> 2. O utilizador seleciona a opção "Criar Tarefa". <br> 3. O sistema exibe um formulário para inserir detalhes da tarefa. <br> 4. O utilizador preenche os campos necessários e confirma a criação. <br> 5. O sistema armazena a tarefa. <br> 6. (Opcional) O utilizador pode atribuir etiquetas ou associar a tarefa a uma pasta. <br> 7. (Opcional) O utilizador pode adicionar a tarefa ao calendário.|
| *Alternative flows and exceptions* | 1. [Erro de validação] Se o utilizador não preencher os campos obrigatórios, o sistema exibe uma mensagem de erro. <br> 2. [Falha ao salvar] Se ocorrer um erro ao salvar a tarefa, o sistema exibe uma notificação e permite tentar novamente. |

### Example: Editar Tarefa
||| 
| --- | --- |
| *Name* | Editar Tarefa |
| *Actor* | Utilizador | 
| *Description* | - O utilizador pode editar uma tarefa já existente no sistema. |
| *Preconditions* | - O utilizador deve estar autenticado. <br> - A tarefa deve existir no sistema. |
| *Postconditions* | - A tarefa é atualizada no sistema com os novos dados. |
| *Normal flow* | 1. O utilizador acede à lista de tarefas. <br> 2. O utilizador seleciona uma tarefa para edição. <br> 3. O sistema exibe os detalhes da tarefa. <br> 4. O utilizador altera os dados necessários. <br> 5. O sistema armazena as alterações. |
| *Alternative flows and exceptions* | 1. [Erro de permissão] Se o utilizador não tiver permissão para editar a tarefa, o sistema bloqueia a ação. <br> 2. [Erro de validação] Se os dados inseridos forem inválidos, o sistema exibe uma mensagem de erro. |

### Example: Eliminar Tarefa
||| 
| --- | --- |
| *Name* | Eliminar Tarefa |
| *Actor* | Utilizador | 
| *Description* | - O utilizador pode remover uma tarefa do sistema. |
| *Preconditions* | - O utilizador deve estar autenticado. <br> - A tarefa deve existir no sistema. |
| *Postconditions* | - A tarefa é removida do sistema e não poderá ser recuperada. |
| *Normal flow* | 1. O utilizador acede à lista de tarefas. <br> 2. O utilizador seleciona uma tarefa para exclusão. <br> 3. O sistema solicita confirmação. <br> 4. O utilizador confirma a ação. <br> 5. O sistema remove a tarefa. |
| *Alternative flows and exceptions* | 1. [Erro de permissão] Se o utilizador não tiver permissão para excluir a tarefa, o sistema bloqueia a ação. |

### Example: Criar Etiqueta
||| 
| --- | --- |
| *Name* | Criar Etiqueta |
| *Actor* | Utilizador | 
| *Description* | - O utilizador pode criar etiquetas para organizar tarefas. |
| *Preconditions* | - O utilizador deve estar autenticado. |
| *Postconditions* | - A nova etiqueta é armazenada no sistema. |
| *Normal flow* | 1. O utilizador acede à seção de etiquetas. <br> 2. O utilizador seleciona a opção "Criar Etiqueta". <br> 3. O sistema exibe um formulário. <br> 4. O utilizador insere um nome para a etiqueta. <br> 5. O sistema armazena a nova etiqueta. |
| *Alternative flows and exceptions* | 1. [Erro de validação] Se o nome da etiqueta for inválido ou já existir, o sistema exibe um erro. |

### Example: Editar Etiqueta
||| 
| --- | --- |
| *Name* | Editar Etiqueta |
| *Actor* | Utilizador | 
| *Description* | - O utilizador pode editar etiquetas existentes. |
| *Preconditions* | - O utilizador deve estar autenticado. <br> - A etiqueta deve existir. |
| *Postconditions* | - A etiqueta é atualizada no sistema. |
| *Normal flow* | 1. O utilizador acede à lista de etiquetas. <br> 2. O utilizador seleciona uma etiqueta para editar. <br> 3. O utilizador altera o nome e salva as mudanças. <br> 4. O sistema armazena as alterações. |
| *Alternative flows and exceptions* | 1. [Erro de permissão] Se o utilizador não tiver permissão para editar etiquetas, o sistema bloqueia a ação. |

### Example: Eliminar Etiqueta
||| 
| --- | --- |
| *Name* | Eliminar Etiqueta |
| *Actor* | Utilizador | 
| *Description* | - O utilizador pode remover etiquetas existentes. |
| *Preconditions* | - O utilizador deve estar autenticado. <br> - A etiqueta deve existir. |
| *Postconditions* | - A etiqueta é removida do sistema. |
| *Normal flow* | 1. O utilizador acede à lista de etiquetas. <br> 2. O utilizador seleciona uma etiqueta para excluir. <br> 3. O sistema solicita confirmação. <br> 4. O utilizador confirma a remoção. <br> 5. O sistema remove a etiqueta. |
| *Alternative flows and exceptions* | 1. [Erro de permissão] Se a etiqueta estiver associada a uma tarefa, o sistema pode impedir a exclusão. |

### Example: Atribuir Etiqueta
||| 
| --- | --- |
| *Name* | Atribuir Etiqueta |
| *Actor* | Utilizador | 
| *Description* | - O utilizador pode associar etiquetas a uma tarefa para facilitar a organização. |
| *Preconditions* | - O utilizador deve estar autenticado. <br> - A tarefa e a etiqueta devem existir. |
| *Postconditions* | - A tarefa fica associada à(s) etiqueta(s) selecionada(s). |
| *Normal flow* | 1. O utilizador acede à lista de tarefas. <br> 2. O utilizador seleciona uma tarefa. <br> 3. O sistema exibe a opção de atribuir etiquetas. <br> 4. O utilizador escolhe uma ou mais etiquetas disponíveis. <br> 5. O sistema salva a associação. |
| *Alternative flows and exceptions* | 1. [Erro de permissão] Se a tarefa pertencer a outro utilizador e houver restrições, a etiqueta pode não ser atribuída. |

### Example: Criar WhitheBoard
||| 
| --- | --- |
| *Name* | Criar Whiteboard |
| *Actor* | Utilizador | 
| *Description* | - O utilizador pode criar um novo quadro colaborativo (Whiteboard). |
| *Preconditions* | - O utilizador deve estar autenticado. |
| *Postconditions* | - O whiteboard é armazenado no sistema. |
| *Normal flow* | 1. O utilizador acede à seção de whiteboards. <br> 2. O utilizador seleciona a opção para criar um novo whiteboard. <br> 3. O sistema cria o whiteboard e permite a edição. <br> 4. O utilizador pode adicionar conteúdo ao quadro. <br> 5. O sistema armazena o novo quadro. |
| *Alternative flows and exceptions* | 1. [Erro de permissão] Se o utilizador não tiver permissão para criar whiteboards, o sistema bloqueia a ação. |

### Example: Editar WhitheBoard
||| 
| --- | --- |
| *Name* | Editar Whiteboard |
| *Actor* | Utilizador | 
| *Description* | - O utilizador pode editar um quadro colaborativo (Whiteboard) existente. |
| *Preconditions* | - O utilizador deve estar autenticado. <br> - O whiteboard deve existir. <br> - O utilizador deve ter permissão para editar o whiteboard. |
| *Postconditions* | - O conteúdo do whiteboard é atualizado no sistema. |
| *Normal flow* | 1. O utilizador acede à seção de whiteboards. <br> 2. O utilizador seleciona um whiteboard existente. <br> 3. O sistema exibe o conteúdo do quadro. <br> 4. O utilizador edita o conteúdo e salva as alterações. <br> 5. O sistema armazena as modificações. |
| *Alternative flows and exceptions* | 1. [Erro de permissão] Se o utilizador não tiver permissão para editar o quadro, o sistema bloqueia a ação. |

### Example: Eliminar WhitheBoard
||| 
| --- | --- |
| *Name* | Eliminar Whiteboard |
| *Actor* | Utilizador | 
| *Description* | - O utilizador pode excluir um quadro colaborativo (Whiteboard). |
| *Preconditions* | - O utilizador deve estar autenticado. <br> - O whiteboard deve existir. <br> - O utilizador deve ter permissão para excluir o whiteboard. |
| *Postconditions* | - O whiteboard é removido do sistema. |
| *Normal flow* | 1. O utilizador acede à seção de whiteboards. <br> 2. O utilizador seleciona um whiteboard para excluir. <br> 3. O sistema solicita confirmação da exclusão. <br> 4. O utilizador confirma a remoção. <br> 5. O sistema exclui o whiteboard. |
| *Alternative flows and exceptions* | 1. [Erro de permissão] Se o utilizador não for dono do quadro, pode não ter permissão para excluir. |

### Example: Atribuir ao Calendário
||| 
| --- | --- |
| *Name* | Atribuir ao Calendário |
| *Actor* | Utilizador | 
| *Description* | - O utilizador pode associar uma tarefa ao calendário. |
| *Preconditions* | - O utilizador deve estar autenticado. <br> - A tarefa deve existir. |
| *Postconditions* | - A tarefa é adicionada ao calendário. |
| *Normal flow* | 1. O utilizador acede a uma tarefa. <br> 2. O utilizador seleciona "Adicionar ao Calendário". <br> 3. O sistema exibe um campo para inserir data e hora. <br> 4. O utilizador confirma a ação. <br> 5. O sistema salva a configuração e adiciona a tarefa ao calendário. |
| *Alternative flows and exceptions* | 1. [Erro de sincronização] Se houver falha ao sincronizar com o Google Calendar, o sistema exibe uma notificação. |

### Example: Criar Alerta
||| 
| --- | --- |
| *Name* | Criar Alertas |
| *Actor* | Utilizador | 
| *Description* | - O utilizador pode configurar alertas para receber notificações sobre uma tarefa. |
| *Preconditions* | - O utilizador deve estar autenticado. <br> - A tarefa deve existir. |
| *Postconditions* | - O utilizador recebe notificações no horário configurado. |
| *Normal flow* | 1. O utilizador acede a uma tarefa. <br> 2. O utilizador seleciona "Criar Alerta". <br> 3. O sistema exibe opções para configurar o alerta (data, hora e tipo de notificação). <br> 4. O utilizador define as configurações desejadas. <br> 5. O sistema armazena as configurações e agenda a notificação. |
| *Alternative flows and exceptions* | 1. [Erro de sincronização] Se houver falha ao sincronizar notificações com o sistema operacional, o sistema exibe uma notificação. |

## Example: Criar Pasta
||| 
| --- | --- |
| *Name* | Criar Pasta |
| *Actor* | Utilizador | 
| *Description* | - O utilizador pode criar pastas para organizar tarefas. |
| *Preconditions* | - O utilizador deve estar autenticado. |
| *Postconditions* | - A nova pasta é armazenada no sistema e pode ser usada para categorizar tarefas. |
| *Normal flow* | 1. O utilizador acede à seção de pastas. <br> 2. O utilizador seleciona a opção "Criar Pasta". <br> 3. O sistema exibe um formulário. <br> 4. O utilizador insere um nome para a pasta. <br> 5. O sistema armazena a nova pasta. |
| *Alternative flows and exceptions* | 1. [Erro de validação] Se o nome da pasta já existir, o sistema exibe um erro. |

### Example: Editar Pasta
||| 
| --- | --- |
| *Name* | Editar Pasta |
| *Actor* | Utilizador | 
| *Description* | - O utilizador pode modificar o nome de uma pasta existente. |
| *Preconditions* | - O utilizador deve estar autenticado. <br> - A pasta deve existir. |
| *Postconditions* | - O nome da pasta é atualizado no sistema. |
| *Normal flow* | 1. O utilizador acede à lista de pastas. <br> 2. O utilizador seleciona uma pasta para editar. <br> 3. O sistema exibe um formulário com o nome atual da pasta. <br> 4. O utilizador altera o nome e confirma. <br> 5. O sistema salva a alteração. |
| *Alternative flows and exceptions* | 1. [Erro de validação] Se o novo nome já existir, o sistema exibe um erro. |

### Example: Eliminar Pasta
||| 
| --- | --- |
| *Name* | Eliminar Pasta |
| *Actor* | Utilizador | 
| *Description* | - O utilizador pode remover uma pasta do sistema. |
| *Preconditions* | - O utilizador deve estar autenticado. <br> - A pasta deve existir. |
| *Postconditions* | - A pasta é removida do sistema, e todas as tarefas associadas ficam sem categoria. |
| *Normal flow* | 1. O utilizador acede à lista de pastas. <br> 2. O utilizador seleciona uma pasta para exclusão. <br> 3. O sistema solicita confirmação. <br> 4. O utilizador confirma a remoção. <br> 5. O sistema remove a pasta. |
| *Alternative flows and exceptions* | 1. [Erro de dependência] Se houver tarefas dentro da pasta, o sistema pode exigir uma confirmação extra para removê-las ou transferi-las. |

### Example: Atribuir Pasta
||| 
| --- | --- |
| *Name* | Atribuir Pasta |
| *Actor* | Utilizador | 
| *Description* | - O utilizador pode associar uma tarefa a uma pasta específica. |
| *Preconditions* | - O utilizador deve estar autenticado. <br> - A tarefa e a pasta devem existir. |
| *Postconditions* | - A tarefa fica categorizada dentro da pasta escolhida. |
| *Normal flow* | 1. O utilizador acede à lista de tarefas. <br> 2. O utilizador seleciona uma tarefa. <br> 3. O sistema exibe a opção de atribuir a uma pasta. <br> 4. O utilizador escolhe uma pasta disponível. <br> 5. O sistema salva a associação. |
| *Alternative flows and exceptions* | 1. [Erro de permissão] Se a tarefa for de outro utilizador, pode não ser possível movê-la. |


---

## Use Case Model / Use Case Table

Criámos um diagrama de casos de uso em UML para representar graficamente os principais casos de uso da aplicação e os atores envolvidos, clarificando o contexto e os limites do sistema. Além disso, elaborámos uma tabela de casos de uso que descreve, de forma detalhada, cada uma das funcionalidades de alto nível, com os respetivos objetivos, atores e descrições, seguindo uma abordagem orientada a resultados (verbo + substantivo). Esta combinação permite uma visão clara e completa das interações esperadas entre os utilizadores e o sistema.

Este é o nosso [Use Case Model](https://github.com/UM-UCs-Org/SOFTWARE-ENGENEERING/blob/main/docs/ModeloCasoSUso.md)

Este é o nossa [Use Case Table](https://github.com/UM-UCs-Org/SOFTWARE-ENGENEERING/blob/main/docs/TabelasCasosdeUso.md)


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

Este são os nossos [Acceptance Tests]https://github.com/UM-UCs-Org/es-2425-tat1/blob/main/docs/TestesAceita%C3%A7%C3%A3o.md

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
