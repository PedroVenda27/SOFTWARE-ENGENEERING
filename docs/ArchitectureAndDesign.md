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

