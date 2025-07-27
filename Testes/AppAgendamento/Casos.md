Funcionalidade: Agendamento de Horário
🔹 Cenário 1 – Agendar horário com nome válido
🎯 Objetivo: Verificar se é possível agendar um horário com o nome preenchido corretamente.

📌 Pré-condição: A data possui horários disponíveis.

🧪 Passos:

Abrir o aplicativo.

Selecionar uma data com horários livres.

Preencher o campo “Nome do cliente”.

Escolher um horário.

Clicar em “Confirmar Agendamento”.

✅ Resultado Esperado: Mostrar mensagem de sucesso e exibir o horário como “Ocupado por [nome]”.

🔹 Cenário 2 – Tentar agendar sem preencher o nome
🎯 Objetivo: Validar que o campo nome é obrigatório.

🧪 Passos:

Escolher uma data e horário.

Deixar o campo “Nome do cliente” vazio.

Clicar em “Confirmar Agendamento”.

✅ Resultado Esperado: Exibir alerta: “Preencha o nome e selecione um horário.”

🔹 Cenário 3 – Visualizar horários ocupados
🎯 Objetivo: Verificar se os horários ocupados aparecem corretamente na interface.

🧪 Passos:

Selecionar uma data com agendamentos.

Observar a lista de horários.

✅ Resultado Esperado: Horários ocupados aparecem como “Ocupado por [nome]” e estão desativados.

🔹 Cenário 4 – Adicionar novo horário no painel de administração
🎯 Objetivo: Confirmar que um novo horário pode ser adicionado corretamente.

🧪 Passos:

Acessar o painel de administração.

Escolher a data desejada.

Inserir um horário no formato correto (ex: 14:30).

Clicar em “Adicionar Horário”.

Salvar.

✅ Resultado Esperado: O horário deve ser adicionado à lista da data selecionada.

🔹 Cenário 5 – Remover horário existente
🎯 Objetivo: Verificar se a remoção de um horário funciona corretamente.

🧪 Passos:

Acessar o painel de administração.

Escolher uma data com horários cadastrados.

Clicar em “Remover” ao lado do horário desejado.

✅ Resultado Esperado: O horário desaparece da lista imediatamente.

🔹 Cenário 6 – Alterar a data e visualizar horários atualizados
🎯 Objetivo: Validar que a lista de horários muda conforme a data escolhida.

🧪 Passos:

Navegar entre as datas.

Verificar a mudança na lista de horários.

✅ Resultado Esperado: A lista atualiza corretamente de acordo com a data.

🔹 Cenário 7 – Validar formato do campo de horário
🎯 Objetivo: Impedir que formatos incorretos sejam aceitos.

🧪 Passos:

Digitar horário inválido (ex: “9999” ou “9h”).

Clicar em “Adicionar Horário”.

✅ Resultado Esperado: Mostrar mensagem de erro indicando o formato correto (HH:MM).


🔹 Teste 8: Impedir agendamento em horário passado
🎯 Objetivo: Verificar se o app impede que o usuário agende um horário em uma data anterior à atual.

📌 Pré-condições:

O dispositivo está com a data e hora atualizadas corretamente.

O usuário está na tela de agendamento.

🧪 Passos de Execução:

Abrir o aplicativo.

Selecionar uma data anterior à data de hoje.

Escolher um horário disponível.

Preencher o nome do cliente.

Clicar em “Confirmar Agendamento”.

🔢 Dados de Entrada:

Data selecionada: 3 dias atrás.

Nome: "Teste Horário Passado"

Horário: 14:00

✅ Resultado Esperado:

O botão de confirmação deve ficar desativado ou

Exibir uma mensagem de erro como: “Não é possível agendar horários em datas passadas.”

O agendamento não deve ser realizado.

🔹 Teste 9: Validar persistência de dados com AsyncStorage
🎯 Objetivo: Verificar se os horários agendados permanecem salvos após o fechamento e reabertura do aplicativo.

📌 Pré-condições:

O aplicativo utiliza AsyncStorage para salvar os agendamentos.

O usuário já realizou um agendamento válido.

🧪 Passos de Execução:

Abrir o aplicativo normalmente.

Selecionar uma data e um horário disponível.

Preencher o campo “Nome do cliente”.

Confirmar o agendamento.

Fechar completamente o app.

Reabrir o aplicativo.

Ir até a mesma data e verificar se o horário aparece como ocupado.

🔢 Dados de Entrada:

Data: hoje

Horário: 10:30

Nome: "Cliente Persistência"

✅ Resultado Esperado:

Ao reabrir o app, o horário deve continuar marcado como “Ocupado por Cliente Persistência”.

A lista de horários deve refletir corretamente os dados salvos anteriormente.

🔹 Teste 10: Validar exibição de mensagens de erro
🎯 Objetivo: Garantir que o aplicativo exiba mensagens de erro adequadas quando o usuário não preenche os campos obrigatórios ou tenta ações inválidas.

📌 Pré-condições:

O usuário está na tela de agendamento.

O sistema possui validação para campos obrigatórios.

🧪 Passos de Execução:

Abrir o app de agendamento.

Selecionar uma data qualquer.

Tentar confirmar o agendamento sem preencher o nome.

Tentar confirmar o agendamento sem selecionar um horário.

Preencher apenas um dos campos e tentar novamente.

Observar a mensagem de retorno exibida pelo sistema.

🔢 Dados de Entrada:

Nome: (vazio)

Horário: (não selecionado)

✅ Resultado Esperado:

Exibir a mensagem: "Preencha o nome e selecione um horário."

O agendamento não deve ser concluído até que os dois campos estejam preenchidos corretamente.


