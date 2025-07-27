Plano de Teste – Aplicativo de Agendamento “Graça Designer”
Autora: Manuela Ramos
Tipo de Teste: Dinâmico / Manual
Técnica: Caixa Preta
Data:24072025
/. Pla/nejamento do Teste
1.1 Objetivos
Verificar se o fluxo de agendamento funciona corretamente.

Confirmar a exibição correta de horários ocupados como "Reservado".

Validar a troca de datas e a atualização da lista de horários.

Garantir a funcionalidade dos botões e campos da interface.

Testar a exibição do nome da cliente na tela administrativa.

1.2 Escopo
Incluído:

Cadastro e reserva de horários por data.

Validação de campos obrigatórios.

Atualização da tela conforme a data selecionada.

Exibição de agendamentos na interface de administração.

Excluído:

Integração com banco de dados externo.

Funcionalidades futuras (notificações, lembretes, login).

1.3 Abordagem
Os testes foram realizados manualmente em ambiente local.

A interface foi testada simulando o comportamento real do usuário.

Casos de teste positivos e negativos foram aplicados.

O código não foi inspecionado (caixa preta).

2. Projeto dos Casos de Teste
2.1 Casos de Teste Positivos
ID	Caso de Teste	Entrada	Resultado Esperado
TC01	Criar horário	15/08 às 10:00	Horário aparece como disponível
TC02	Agendar horário	Nome: Ana, Data: 15/08, Hora: 10:00	Horário marcado como "Reservado"
TC03	Trocar data	Alterar para 16/08	Lista mostra horários dessa data
TC04	Ver gerenciamento	Tela de administração	Mostrar nome “Ana” no horário reservado
TC05	Agendar dois horários	Nome: Bruna, 09:00 e 14:00	Ambos os horários salvos como reservados

2.2 Casos de Teste Negativos
ID	Caso de Teste	Entrada	Resultado Esperado
TC06	Agendar sem horário	Nome preenchido, horário não	Mensagem de erro exibida
TC07	Nome vazio	Data e horário preenchidos	Impedir agendamento, exibir aviso
TC08	Agendar horário ocupado	Selecionar horário já reservado	Exibir mensagem: “Horário indisponível”
TC09	Inserir caracteres inválidos	Nome: "!!!@@@"	Campo não aceita, ou exibe aviso
TC10	Criar horário sem data	Clicar em "Adicionar horário"	Exibir erro de campo obrigatório

3. Execução do Teste
3.1 Execução Manual
A usuária acessou o app simulando a cliente e a administradora.

Foram preenchidos dados reais e fictícios.

As respostas do sistema foram comparadas com os resultados esperados.

Foram feitas capturas de tela em testes com falha.

3.2 Documentação de Defeitos
ID	Descrição	Severidade	Status
DEF01	Horário reservado ainda aparece como disponível após agendamento	Alta	Corrigido
DEF02	Campo de nome aceita símbolos como "###"	Média	Pendente
DEF03	Botão "Clear" não limpa corretamente os campos	Baixa	Corrigido

4. Avaliação do Teste
4.1 Análise de Defeitos
Defeitos de cálculo e reserva foram tratados como críticos.

Questões de entrada inválida foram marcadas como médias.

Pequenos problemas visuais foram baixa severidade.

4.2 Tomada de Decisão
Defeitos críticos foram corrigidos imediatamente antes de nova rodada de testes.

Problemas de baixa severidade serão considerados em melhorias futuras.

✅ Conclusão
O plano de teste mostrou que o app está funcional para o uso básico de agendamento. Foram identificadas melhorias de validação de campos, que podem ser aplicadas em próximas versões. Esse processo reforça o uso de testes manuais com abordagem de caixa preta para validar sistemas reais.

