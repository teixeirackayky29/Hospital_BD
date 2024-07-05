# Hospital_BD
# 01 O Hospital Fundamental. 

Mãos a Obra
Analise a seguinte descrição e extraia dela os requisitos para o banco de dados:
O hospital necessita de um sistema para sua área clínica que ajude a controlar consultas realizadas. Os médicos podem ser generalistas, especialistas ou residentes e têm seus dados pessoais cadastrados em planilhas digitais. Cada médico pode ter uma ou mais especialidades, que podem ser pediatria, clínica geral, gastroenterologia e dermatologia. Alguns registros antigos ainda estão em formulário de papel, mas será necessário incluir esses dados no novo sistema.

Os pacientes também precisam de cadastro, contendo dados pessoais (nome, data de nascimento, endereço, telefone e e-mail), documentos (CPF e RG) e convênio. Para cada convênio, são registrados nome, CNPJ e tempo de carência.

As consultas também têm sido registradas em planilhas, com data e hora de realização, médico responsável, paciente, valor da consulta ou nome do convênio, com o número da carteira. Também é necessário indicar na consulta qual a especialidade buscada pelo paciente.

Deseja-se ainda informatizar a receita do médico, de maneira que, no encerramento da consulta, ele possa registrar os medicamentos receitados, a quantidade e as instruções de uso. A partir disso, espera-se que o sistema imprima um relatório da receita ao paciente ou permita sua visualização via internet.


![Captura de tela 2024-07-04 234956](https://github.com/teixeirackayky29/Hospital_BD/assets/95193248/9592a491-3f64-4ad4-803f-020ac78574b9)

# 02 Os Segredos do Hospital

Entender do assunto
Considere a seguinte descrição e o diagrama ER abaixo:

No hospital, as internações têm sido registradas por meio de formulários eletrônicos que gravam os dados em arquivos. 

Para cada internação, são anotadas a data de entrada, a data prevista de alta e a data efetiva de alta, além da descrição textual dos procedimentos a serem realizados. 

As internações precisam ser vinculadas a quartos, com a numeração e o tipo. 

Cada tipo de quarto tem sua descrição e o seu valor diário (a princípio, o hospital trabalha com apartamentos, quartos duplos e enfermaria).

Também é necessário controlar quais profissionais de enfermaria estarão responsáveis por acompanhar o paciente durante sua internação. Para cada enfermeiro(a), é necessário nome, CPF e registro no conselho de enfermagem (CRE).

A internação, obviamente, é vinculada a um paciente – que pode se internar mais de uma vez no hospital – e a um único médico responsável.

# Mãos a obra?

Faça a ligação do diagrama acima ao diagrama desenvolvido na atividade antrior, construindo relacionamentos com entidades relacionadas. E eleve o seu diagrama para que já selecionando os tipos de dados que serão trabalhados e em quais situações. 

Por último, crie um script SQL para a geração do banco de dados e para instruções de montagem de cada uma das entidades/tabelas presentes no diagrama completo (considerando as entidades do diagrama da atividade anterior e as novas entidades propostas no diagrama acima). Também crie tabelas para relacionamentos quando necessário. Aplique colunas e chaves primárias e estrangeiras.
Use ferramentas, como ERPlus, Lucidchart, draw.io (via web) e MySQL Workbench, ou mesmo um editor de imagens para o diagrama. 

Você pode utilizar o MySQL Workbench ou o DBdiagram.io para montar os scripts SQL.

![Captura de tela 2024-07-05 013305](https://github.com/teixeirackayky29/Hospital_BD/assets/95193248/15501263-eac5-431a-8bc7-de765748cd8e)

# 03 O Prisioneiro de dados

Jogando nas regras que você criou: 
Crie scripts de povoamento das tabelas desenvolvidas na atividade anterior
Observe as seguintes atividades: 
Inclua ao menos dez médicos de diferentes especialidades.

Ao menos sete especialidades (considere a afirmação de que “entre as especialidades há pediatria, clínica geral, gastrenterologia e dermatologia”).

Inclua ao menos 15 pacientes.

Registre 20 consultas de diferentes pacientes e diferentes médicos (alguns pacientes realizam mais que uma consulta). As consultas devem ter ocorrido entre 01/01/2015 e 01/01/2022. Ao menos dez consultas devem ter receituário com dois ou mais medicamentos.

Inclua ao menos quatro convênios médicos, associe ao menos cinco pacientes e cinco consultas.

Criar entidade de relacionamento entre médico e especialidade. 

Criar Entidade de Relacionamento entre internação e enfermeiro. 

Arrumar a chave estrangeira do relacionamento entre convênio e médico.

Criar entidade entre internação e enfermeiro.

Colocar chaves estrangeira dentro da internação (Chaves Médico e Paciente).

Registre ao menos sete internações. Pelo menos dois pacientes devem ter se internado mais de uma vez. Ao menos três quartos devem ser cadastrados. As internações devem ter ocorrido entre 01/01/2015 e 01/01/2022.

Considerando que “a princípio o hospital trabalha com apartamentos, quartos duplos e enfermaria”, inclua ao menos esses três tipos com valores diferentes.

Inclua dados de dez profissionais de enfermaria. Associe cada internação a ao menos dois enfermeiros.

Os dados de tipo de quarto, convênio e especialidade são essenciais para a operação do sistema e, portanto, devem ser povoados assim que o sistema for instalado.

# 04 A Ordem do Alterar. 

Mãos a Obra. 
Pensando no banco que já foi criado para o Projeto do Hospital, realize algumas alterações nas tabelas e nos dados usando comandos de atualização e exclusão:

Crie um script que adicione uma coluna “em_atividade” para os médicos, indicando se ele ainda está atuando no hospital ou não. 

Crie um script para atualizar ao menos dois médicos como inativos e os demais em atividade.

![Captura de tela 2024-07-05 015723](https://github.com/teixeirackayky29/Hospital_BD/assets/95193248/5d759964-1c49-4891-9986-b64108c34248)

# 05 As Relíquias dos Dados

Mãos a obra
Crie um script e nele inclua consultas que retornem:

-- Consulta 1: Todos os dados e valor médio das consultas do ano de 2020 e das que foram feitas sob convênio

![image](https://github.com/teixeirackayky29/Hospital_BD/assets/95193248/89069ad0-72af-487c-b133-e0bebe284fa5)

-- Consulta 2: Todos os dados das internações que tiveram data de alta maior que a data prevista para a alta

![image](https://github.com/teixeirackayky29/Hospital_BD/assets/95193248/16731714-0fd4-49c4-9c36-0c8e2370eefc)

-- Consulta 3: Receituário completo da primeira consulta registrada com receituário associado

![image](https://github.com/teixeirackayky29/Hospital_BD/assets/95193248/a5da071b-eb39-4aa1-b4f0-d174f3173964)

-- Consulta 4: Todos os dados da consulta de maior valor e também da de menor valor (ambas as consultas não foram realizadas sob convênio)

![image](https://github.com/teixeirackayky29/Hospital_BD/assets/95193248/fd754c1a-35d1-4030-9ea9-c16be3582a13)

-- Consulta 5: Todos os dados das internações em seus respectivos quartos, calculando o total da internação a partir do valor de diária do quarto e o número de dias entre a entrada e a alta

![image](https://github.com/teixeirackayky29/Hospital_BD/assets/95193248/91a22700-39cd-4f78-b746-21dee197831d)

-- Consulta 6: Data, procedimento e número de quarto de internações em quartos do tipo “apartamento”

![image](https://github.com/teixeirackayky29/Hospital_BD/assets/95193248/50f9d894-77eb-4d14-978c-d0d29887cddc)

-- Consulta 7: Nome do paciente, data da consulta e especialidade de todas as consultas em que os pacientes eram menores de 18 anos na data da consulta e cuja especialidade não seja “pediatria”, ordenando por data de realização da consulta

![image](https://github.com/teixeirackayky29/Hospital_BD/assets/95193248/def4ef97-14f3-42aa-b3ab-74d0f522284d)

-- Consulta 8: Nome do paciente, nome do médico, data da internação e procedimentos das internações realizadas por médicos da especialidade “gastroenterologia”, que tenham acontecido em “enfermaria”

![image](https://github.com/teixeirackayky29/Hospital_BD/assets/95193248/6e23d707-fb6f-4e1f-a5bc-b884739382f4)

-- Consulta 9: Os nomes dos médicos, seus CRMs e a quantidade de consultas que cada um realizou

![image](https://github.com/teixeirackayky29/Hospital_BD/assets/95193248/e4c101ff-9c37-404e-808c-ceeb8e6b7ce0)

-- Consulta 10: Todos os médicos que tenham "Gabriel" no nome

![image](https://github.com/teixeirackayky29/Hospital_BD/assets/95193248/ffe804c3-9716-4186-8adf-0fd93864f6c1)

-- Consulta 11: Os nomes, CREs e número de internações de enfermeiros que participaram de mais de uma internação

![image](https://github.com/teixeirackayky29/Hospital_BD/assets/95193248/9d0a64b9-ab33-4e4e-aa26-c3fe5cb66050)










