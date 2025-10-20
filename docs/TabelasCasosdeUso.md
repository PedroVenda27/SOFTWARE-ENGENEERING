### Tabelas Casos De Uso


## Example: Criar Tarefa
|||
| --- | --- |
| *Name* | Criar Tarefa |
| *Actor* | Utilizador | 
| *Description* |- O utilizador cria uma nova tarefa no sistema, podendo atribuir etiquetas, pastas e associá-la ao calendário. |
| *Preconditions* | - O utilizador deve estar autenticado no sistema. <br> - O utilizador deve ter permissão para criar tarefas. |
| *Postconditions* | - Se atribuída ao calendário, a tarefa aparece na agenda. <br> - Se tiver etiquetas ou pastas, a tarefa fica associada a elas. |
| *Normal flow* | 1. O utilizador acede ao sistema. <br> 2. O utilizador seleciona a opção "Criar Tarefa". <br> 3. O sistema exibe um formulário para inserir detalhes da tarefa. <br> 4. O utilizador preenche os campos necessários e confirma a criação. <br> 5. O sistema armazena a tarefa. <br> 6. (Opcional) O utilizador pode atribuir etiquetas ou associar a tarefa a uma pasta. <br> 7. (Opcional) O utilizador pode adicionar a tarefa ao calendário.|
| *Alternative flows and exceptions* | 1. [Erro de validação] Se o utilizador não preencher os campos obrigatórios, o sistema exibe uma mensagem de erro. <br> 2. [Falha ao salvar] Se ocorrer um erro ao salvar a tarefa, o sistema exibe uma notificação e permite tentar novamente. |

## Example: Editar Tarefa
||| 
| --- | --- |
| *Name* | Editar Tarefa |
| *Actor* | Utilizador | 
| *Description* | - O utilizador pode editar uma tarefa já existente no sistema. |
| *Preconditions* | - O utilizador deve estar autenticado. <br> - A tarefa deve existir no sistema. |
| *Postconditions* | - A tarefa é atualizada no sistema com os novos dados. |
| *Normal flow* | 1. O utilizador acede à lista de tarefas. <br> 2. O utilizador seleciona uma tarefa para edição. <br> 3. O sistema exibe os detalhes da tarefa. <br> 4. O utilizador altera os dados necessários. <br> 5. O sistema armazena as alterações. |
| *Alternative flows and exceptions* | 1. [Erro de permissão] Se o utilizador não tiver permissão para editar a tarefa, o sistema bloqueia a ação. <br> 2. [Erro de validação] Se os dados inseridos forem inválidos, o sistema exibe uma mensagem de erro. |

## Example: Eliminar Tarefa
||| 
| --- | --- |
| *Name* | Eliminar Tarefa |
| *Actor* | Utilizador | 
| *Description* | - O utilizador pode remover uma tarefa do sistema. |
| *Preconditions* | - O utilizador deve estar autenticado. <br> - A tarefa deve existir no sistema. |
| *Postconditions* | - A tarefa é removida do sistema e não poderá ser recuperada. |
| *Normal flow* | 1. O utilizador acede à lista de tarefas. <br> 2. O utilizador seleciona uma tarefa para exclusão. <br> 3. O sistema solicita confirmação. <br> 4. O utilizador confirma a ação. <br> 5. O sistema remove a tarefa. |
| *Alternative flows and exceptions* | 1. [Erro de permissão] Se o utilizador não tiver permissão para excluir a tarefa, o sistema bloqueia a ação. |

## Example: Criar Etiqueta
||| 
| --- | --- |
| *Name* | Criar Etiqueta |
| *Actor* | Utilizador | 
| *Description* | - O utilizador pode criar etiquetas para organizar tarefas. |
| *Preconditions* | - O utilizador deve estar autenticado. |
| *Postconditions* | - A nova etiqueta é armazenada no sistema. |
| *Normal flow* | 1. O utilizador acede à seção de etiquetas. <br> 2. O utilizador seleciona a opção "Criar Etiqueta". <br> 3. O sistema exibe um formulário. <br> 4. O utilizador insere um nome para a etiqueta. <br> 5. O sistema armazena a nova etiqueta. |
| *Alternative flows and exceptions* | 1. [Erro de validação] Se o nome da etiqueta for inválido ou já existir, o sistema exibe um erro. |

## Example: Editar Etiqueta
||| 
| --- | --- |
| *Name* | Editar Etiqueta |
| *Actor* | Utilizador | 
| *Description* | - O utilizador pode editar etiquetas existentes. |
| *Preconditions* | - O utilizador deve estar autenticado. <br> - A etiqueta deve existir. |
| *Postconditions* | - A etiqueta é atualizada no sistema. |
| *Normal flow* | 1. O utilizador acede à lista de etiquetas. <br> 2. O utilizador seleciona uma etiqueta para editar. <br> 3. O utilizador altera o nome e salva as mudanças. <br> 4. O sistema armazena as alterações. |
| *Alternative flows and exceptions* | 1. [Erro de permissão] Se o utilizador não tiver permissão para editar etiquetas, o sistema bloqueia a ação. |

## Example: Eliminar Etiqueta
||| 
| --- | --- |
| *Name* | Eliminar Etiqueta |
| *Actor* | Utilizador | 
| *Description* | - O utilizador pode remover etiquetas existentes. |
| *Preconditions* | - O utilizador deve estar autenticado. <br> - A etiqueta deve existir. |
| *Postconditions* | - A etiqueta é removida do sistema. |
| *Normal flow* | 1. O utilizador acede à lista de etiquetas. <br> 2. O utilizador seleciona uma etiqueta para excluir. <br> 3. O sistema solicita confirmação. <br> 4. O utilizador confirma a remoção. <br> 5. O sistema remove a etiqueta. |
| *Alternative flows and exceptions* | 1. [Erro de permissão] Se a etiqueta estiver associada a uma tarefa, o sistema pode impedir a exclusão. |

## Example: Atribuir Etiqueta
||| 
| --- | --- |
| *Name* | Atribuir Etiqueta |
| *Actor* | Utilizador | 
| *Description* | - O utilizador pode associar etiquetas a uma tarefa para facilitar a organização. |
| *Preconditions* | - O utilizador deve estar autenticado. <br> - A tarefa e a etiqueta devem existir. |
| *Postconditions* | - A tarefa fica associada à(s) etiqueta(s) selecionada(s). |
| *Normal flow* | 1. O utilizador acede à lista de tarefas. <br> 2. O utilizador seleciona uma tarefa. <br> 3. O sistema exibe a opção de atribuir etiquetas. <br> 4. O utilizador escolhe uma ou mais etiquetas disponíveis. <br> 5. O sistema salva a associação. |
| *Alternative flows and exceptions* | 1. [Erro de permissão] Se a tarefa pertencer a outro utilizador e houver restrições, a etiqueta pode não ser atribuída. |

## Example: Criar WhitheBoard
||| 
| --- | --- |
| *Name* | Criar Whiteboard |
| *Actor* | Utilizador | 
| *Description* | - O utilizador pode criar um novo quadro colaborativo (Whiteboard). |
| *Preconditions* | - O utilizador deve estar autenticado. |
| *Postconditions* | - O whiteboard é armazenado no sistema. |
| *Normal flow* | 1. O utilizador acede à seção de whiteboards. <br> 2. O utilizador seleciona a opção para criar um novo whiteboard. <br> 3. O sistema cria o whiteboard e permite a edição. <br> 4. O utilizador pode adicionar conteúdo ao quadro. <br> 5. O sistema armazena o novo quadro. |
| *Alternative flows and exceptions* | 1. [Erro de permissão] Se o utilizador não tiver permissão para criar whiteboards, o sistema bloqueia a ação. |

## Example: Editar WhitheBoard
||| 
| --- | --- |
| *Name* | Editar Whiteboard |
| *Actor* | Utilizador | 
| *Description* | - O utilizador pode editar um quadro colaborativo (Whiteboard) existente. |
| *Preconditions* | - O utilizador deve estar autenticado. <br> - O whiteboard deve existir. <br> - O utilizador deve ter permissão para editar o whiteboard. |
| *Postconditions* | - O conteúdo do whiteboard é atualizado no sistema. |
| *Normal flow* | 1. O utilizador acede à seção de whiteboards. <br> 2. O utilizador seleciona um whiteboard existente. <br> 3. O sistema exibe o conteúdo do quadro. <br> 4. O utilizador edita o conteúdo e salva as alterações. <br> 5. O sistema armazena as modificações. |
| *Alternative flows and exceptions* | 1. [Erro de permissão] Se o utilizador não tiver permissão para editar o quadro, o sistema bloqueia a ação. |

## Example: Eliminar WhitheBoard
||| 
| --- | --- |
| *Name* | Eliminar Whiteboard |
| *Actor* | Utilizador | 
| *Description* | - O utilizador pode excluir um quadro colaborativo (Whiteboard). |
| *Preconditions* | - O utilizador deve estar autenticado. <br> - O whiteboard deve existir. <br> - O utilizador deve ter permissão para excluir o whiteboard. |
| *Postconditions* | - O whiteboard é removido do sistema. |
| *Normal flow* | 1. O utilizador acede à seção de whiteboards. <br> 2. O utilizador seleciona um whiteboard para excluir. <br> 3. O sistema solicita confirmação da exclusão. <br> 4. O utilizador confirma a remoção. <br> 5. O sistema exclui o whiteboard. |
| *Alternative flows and exceptions* | 1. [Erro de permissão] Se o utilizador não for dono do quadro, pode não ter permissão para excluir. |

## Example: Atribuir ao Calendário
||| 
| --- | --- |
| *Name* | Atribuir ao Calendário |
| *Actor* | Utilizador | 
| *Description* | - O utilizador pode associar uma tarefa ao calendário. |
| *Preconditions* | - O utilizador deve estar autenticado. <br> - A tarefa deve existir. |
| *Postconditions* | - A tarefa é adicionada ao calendário. |
| *Normal flow* | 1. O utilizador acede a uma tarefa. <br> 2. O utilizador seleciona "Adicionar ao Calendário". <br> 3. O sistema exibe um campo para inserir data e hora. <br> 4. O utilizador confirma a ação. <br> 5. O sistema salva a configuração e adiciona a tarefa ao calendário. |
| *Alternative flows and exceptions* | 1. [Erro de sincronização] Se houver falha ao sincronizar com o Google Calendar, o sistema exibe uma notificação. |

## Example: Criar Alerta
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

## Example: Editar Pasta
||| 
| --- | --- |
| *Name* | Editar Pasta |
| *Actor* | Utilizador | 
| *Description* | - O utilizador pode modificar o nome de uma pasta existente. |
| *Preconditions* | - O utilizador deve estar autenticado. <br> - A pasta deve existir. |
| *Postconditions* | - O nome da pasta é atualizado no sistema. |
| *Normal flow* | 1. O utilizador acede à lista de pastas. <br> 2. O utilizador seleciona uma pasta para editar. <br> 3. O sistema exibe um formulário com o nome atual da pasta. <br> 4. O utilizador altera o nome e confirma. <br> 5. O sistema salva a alteração. |
| *Alternative flows and exceptions* | 1. [Erro de validação] Se o novo nome já existir, o sistema exibe um erro. |

## Example: Eliminar Pasta
||| 
| --- | --- |
| *Name* | Eliminar Pasta |
| *Actor* | Utilizador | 
| *Description* | - O utilizador pode remover uma pasta do sistema. |
| *Preconditions* | - O utilizador deve estar autenticado. <br> - A pasta deve existir. |
| *Postconditions* | - A pasta é removida do sistema, e todas as tarefas associadas ficam sem categoria. |
| *Normal flow* | 1. O utilizador acede à lista de pastas. <br> 2. O utilizador seleciona uma pasta para exclusão. <br> 3. O sistema solicita confirmação. <br> 4. O utilizador confirma a remoção. <br> 5. O sistema remove a pasta. |
| *Alternative flows and exceptions* | 1. [Erro de dependência] Se houver tarefas dentro da pasta, o sistema pode exigir uma confirmação extra para removê-las ou transferi-las. |

## Example: Atribuir Pasta
||| 
| --- | --- |
| *Name* | Atribuir Pasta |
| *Actor* | Utilizador | 
| *Description* | - O utilizador pode associar uma tarefa a uma pasta específica. |
| *Preconditions* | - O utilizador deve estar autenticado. <br> - A tarefa e a pasta devem existir. |
| *Postconditions* | - A tarefa fica categorizada dentro da pasta escolhida. |
| *Normal flow* | 1. O utilizador acede à lista de tarefas. <br> 2. O utilizador seleciona uma tarefa. <br> 3. O sistema exibe a opção de atribuir a uma pasta. <br> 4. O utilizador escolhe uma pasta disponível. <br> 5. O sistema salva a associação. |
| *Alternative flows and exceptions* | 1. [Erro de permissão] Se a tarefa for de outro utilizador, pode não ser possível movê-la. |
