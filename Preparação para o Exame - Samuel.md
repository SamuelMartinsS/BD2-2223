
**Q1** Qual a diferença entre uma #View e #Materialzed_View ?

	As views são representações virtuais de uma tabela. Sempre que uma view é consultada, a consulta subjacente é exxecutada e os resultados são devolvidos. 
	As Materialized views são cópias fisicas de uma view. Os seus dados são armazenados no armazenamento do PC.
	A diferença entre as views e as materialized é que enquanto uma view é atualizada dinamicamente sempre que é consultada, as materialized views precisam de ser atualizadas.
	As materialized views poodem aumtentar o desempenho da base de dados caso sejam necessárioss consultas bastante frequentes ou complexas porque estes dados já estão guardados.

**Q2** Diferenças entre o #Docker e #Maquinas_virtuais ?

	O docker é utilizado para guardar contentores leves para guardar.
	As máquinas virtuais são utilizadas para emular um computador separado com sistema operativo funcional. 
	O Docker é mais adequado para pequenos serviços que possam ser rapidamente inicializados como por exemplo para guardar bases de dados, equanto que as máquinas virtuais são utilizadas principalmente para simular PCs.
	
**Q3** O que são #Tokens e para que servem ?

	Os tokens são um conjunto de carateres que contem algumas informações codificadas. Estes são utilizados para realizar autenticação em determinados endpoints de uma API, como por exemplo, para realizar Logout. Algumas das informações que um Token pode conter são o ID do utilizador, a data de expiração e o grupo a que o utilizador pertence.

**Q4** Medidas de #segurança que as bases de dados devem ter ?

	Algumas das medidas de segurança que devem ser implementadas numa base de dados são o controlo de acesso, ou seja, os dados devem estar protegidos e restritos apenas a pessoal que está autorizado a consultar ou edita-los, monitorização, devem ser guardadas as ações que são realizadas com os dados contidos na base de dados e todas as ações dos utilizadores para garantir a maxima segurança. Backups, devem ser implentados backups para garantir que, caso a base de dados seja perdida, seja possivel recuperar os dados.

**Q5** O que é #SQL_injenction e formas de evitar ?

	SQL injections são feitos através da inserção de partes de uma query em caixas de texto, por exemplo, que não estejam devidamente protegidas com o objetivo de manipular as query pré-existentes de forma a evitar ou ignorar determinadas condições ou até mesmo para eliminar a base de dados em casos extremos. Uma forma de evitar SQL injection é a utilização de prepared statements, garantir poucos ou nenhums privilégios a outros utilizadores ou utilização de validações para evitar expressões como 'Drop table', por exemplo.
	
**Q6** Qual o motivo pelo qual se deve utilizar #Views ?

	As views são utilizadas para proporcionar abstração de elementos da base de dados. Estas podem ser utilizadas como um meio de segurança de dados restringindo o acesso direto a tabelas da base de dados.
	Para alem da segurança, as views são utilizadas para uma melhoria de desempenho das consultas. 
	
**Q7** #Rules e #Trigger e que são, onde se devem utilizar e diferenças ?

	As rules são instruções que são executadas automaticamente em resposta a uma ação na base de dados.
	Estas, estão associadas a uma tabela da base de dados.
	Os triggers são regras que são estabelecidas para responder a ações especificas na base de dados. Estes estão associados a uma tabela e apenas são executados quando quando ocorrer uma determinada condição que deve ser definida no trigger. Para além destas diferenças, os triggers são bastante mais flexiveis e podem ser adaptados a uma maior variedade de situações.

**Q8** O que são #Cursores, onde se devem utilizar e para quê ?

	Os cursores são estruturas que permitem amnipular um conjunto de dados retornados por uma consulta.
	Estes são utilizados quando é necessário percorrer um conjunto de dados para lhes aplicar um deeterminado algoritmo a cada registo individual do conjunto devolvido.

**Q9** #Registos de tamanho de variável ?

	Os registos de tamanho fixo são utilizados para guardar dados de vários tamanhos de uma forma rápida.
	Apesar de serem bastante uteis devido à sua flexibilidade, apenas devem ser utilizados em situações quando o tamanho dos dados pode variar de uma forma radical, caso contrário, devem ser utilizados registos de tamanhos fixos.

**Q10** Quais são os problemas de utilizar #Registo de tamanho variável ?

	Ao utilizar registos dinâmicos, estes vão consumir mais memória do que registos de tamanho fixo. Por isso, apenas devem ser utilizados em situações expecificas.

**Q11** Que tipos de #Registo se deve utilizar para guardar objetos de #grande dimensão na base de dados e quais os #problemas de os guardar ?

	Podem ser utilizados registos de tamanho variavel ou estático, dependendo se o tamanho destes varia muito ou não. Ao guardar elementos com grande tamannho, isto pode causar uma perda de desempenho. Para além da possivel perda de desempenho, a escalabilidade da base e dados passa a ser um desafio assim como a complexidade na modelagem da mesma. Por essas causas, os arquivos de grande volume podem ser guardados em ficheiros, isto torna o armazenamento mais eficiente, mais rápido, consistente e permite que sejam compartilhados mais facilmente.


**Q12** Motivo da organização de #Registos em ficheiros ?

	A organização de registos em ficheiros deve ser utilizada em dados de grande volume. Isto permite que sejam mais facilmente guardados, garante um acessoa mais rápido, eficiente e consistente, e possibilita a partilha destes ficheiros de uma forma mais facil.
	 
**Q13** O que são #Índices densos e espaçados ?

	Indices densos são criados de tal forma que têm um ponteiro que está direcionado par acada linha da tabela, ou seja, quando é criado, cada linha da tabela vai estar ter como correspondencia um ponteiro pertencente ao indice denso criado para essa tabela. Estes indices facilitam a localização rápida de registos.
	Os Indices espaçados são criados para apenas um subconjunto selecionado de valores, por isso, quando são criados, vão existir sempre menos indices do que o numero de linhas de uma tabela. Este tipo de indices é eficiente quando existem vários valores repetidos numa coluna que tenha sido indexada popis não é necessário criar uma entrada para cada ocorrencia, por exemplo.

**Q14** Em #postgres como podem ser gerados dados sintéticos ?

	Dados sintéticos, são dados criados artificalmente que se assemelham a dados reais. Estes são utilizados para realizar uma grande variedade de testes.
	Os dados sintéticos podem ser criados através de funções como random(), para gerar valores aleatorios, generate_series(), para gerar uma series de valores numéricos sequenciais ou recorrendo a  extensões como pg_fake_data que fornece uma variedade de funções para gerar dados sintéticos.
	
**Q15** Para que serve o #Explain ?

	O explain é uma ferramente que tem como objetivo indicar o desempenho de consultas em SQL, a partir dos resultados obtidos podem ser retiradas várias conclusões sobre a otimização de uma query.

**Q16** Como são criados os #Índices ?

	Para criar um index é utilizada a seguinte syntax:
	CREATE INDEX [nome do indice] ON [nome da tabela] (coluna);

**Q17** Quais as dois principais papeis de um #administrador de uma base de dados ?

	O administrador de uma base de dados tem vários papeis. Entre esses, destacam-se os papeis de gestor e técnico. Os adminstradores de bases de dados devem estar atentos a atualizações que são feitas na base de dados, é o responsavevl por configurar o sistema e de assegurar o bom funcionamento do mesmo. Deve tambem fazer o monitoramento do desempenho e realizar a otimização sempre que necessário. Para além dos papeis referidos anteriormente, o admnistrador deve tambem realizar backups e e assegurar-se que a base de dados está segura e atualizada para que não sejam corridos riscos de perder informações.w2

**Q18** Boas regras na geração de #backups, tipo de backups ?

	Quando é realizado um backup, deve ser tomado em conta os seguintes aspetos:
	Qual a estratégia de backup mais adequada para a situação, de quanto em quanto tempo deve ser realizado o backup e agendar previamente datas quando vão ser realizados os backups, testar a recuperação de backups para garantir a integridade dos dados e manter várias versões históricas de backups em caso de ocorrer uma perda catastrófica.
	
**Q19** Que #ferramentas de administração da base de dados existem ?

	Algumas ferramentas que podem ser utilizadas para administrar uma base de dados é por exemplo, pgAdmin, mySQL workbench, heidiSQL ou Oracle Manager. Todas estas ferramentas são adequadas para gerir e administrar bases de dados.

**Q20** #Table_spaces o que são e como se relacionam na criação de base de dados ?

	Table spaces é um local fisico no sistema onde estão guardados dados de uma tabela.
	Os Table spaces são utilizados por vários motivos, nomeadamente para gerenciamento do vários dados armazenados, manutenção de partes especificas da base de dados.

**Q21** #Schemas, o que são e para q servem ?

	Schemas é são estruturas que organizam e agrupam objetos que estejam relacionados, como  tabelas, views, funções e procedimentos, por exemplo. Estas são utilizadas, para uma organizar a base de dados de forma a facilitar a navegação e compreensão da mesma e também para controlar o acesso aos dados dando acesso, ou não aos vários utilizadores.

**Q22** #Segurança de base de dados, e quais os parâmetros principais ?

	Algumas das medidas de principais medidas de segurança numa base de dados, são o controlo de acesso, devem ser criados utilizadores ou grupos de utilizadores e atribuir apenas as permissões necessárias. Encriptação de informações sensiveis ou importantes que sejam guardadas na base de dados, como passwords, por exemplo. A realização de backups para permitir a recuperação dos dados caso acontece algo catastrófico à base de dados. Devem tambem ser feitas monitorizações do desempenho e da atividade na base de dados. 

**Q23** Boas práticas na segurança de #passwords ?

	Para guardar passwords numa base de dados, devem ser seguidas algumas regras para garantir segurança. Algumas dessas regras passam por utilizar algoritmos de encriptação, devem ser utilizados algoritmos de encriptação, utilização de rules que apenas permitam passwords com um minimo de carateres de comprimento e com determinadas condições como letras maiusculas, numeros e carateres, por exemplo. Param alem das anteriores, deve ser feito o monitoramento à base de dados para garantir que não ocorrem ataques que possam afetar a segurança das passwords.

**Q24** Em que consiste o #salt na criação da #password ?

	O método salt tem como objetivo aumentara segurança no armazenamento de senhas numa base de dados, encriptando-as. O valor gerado pelo salt é gerado numa forma aleatoria e possui, normalmente, um tamanho fixo. Este é concatenado à senha do utilizador antes da encriptação e depois passa por uma função de hashing que acaba por gerar um resultado unico.

**Q25** Em que consiste a #Auditoria de base de dados ?

	A auditoria numa base de dados passa por vários eventos, como registar as informações de acesso e de autenticação à base de dados para controlar quem acessa aos dados e o que faz com eles, informações acerca de operações de consulta e escrita na base de dados e eventos de segurança, de erros e excepções.
	A auditoria é bastante importante não só por motivos de segurança, mas tambem para identificar problemas e formas de os resolver.

**Q26** Que tipos de #Privilegios existem na base de dados ?

	Existem várias permissões e privilégios que podem ser garantidos a utilizadores ou grupos numa base de dados. Alguns destes privilégios são de sistema, que consistem em permissões globais da base de dados que incluem a CREATE e DROP, privilégios de manipulação de dados, que consiste em SELECT, INSERT, UPDATE, entre outros... , privilégios de schemas que permitem a criação, alteração e utilização de schemas e finalmente o privilégio de garantir ou remover privilégios a outros utilizadores, estes que devem ser utilizados pelos administradores da base de dados. 

**Q27** #JWT, em que consiste o #encode e #decode ?

	JWT significa JSON Web Token e é um padrão que define um formato autossuficiente para transmitir informações de forma segura.
	O JWT é constituido por duas 3 partes separadas por pontos, o Header que contem informação sobre o tipo de token e  o algoritmo utilizador, o Payload que contem informações sobre o utilizador e outras adicionais, e finalmente a Signature que é utilizado para verificar a validade do token.
	O processo de encoding consiste em construir um Header e o Payload e codifica-lo utilizando Base64 e por fim a Signature é gerada e adicionada.
	O processo de decoding consiste na analise do token. Este método consiste em descodificar o JWT, recorrendo a Base64, e validar a Signature do token para verificar a sua integridade.

**Q28** O que são ferramentas #OLAP ?

	Ferramentas OLAP são utilizadas para analise e exploração de dados numa base de dados. Estas são ferramentas projetadas para auxiliar os administradores a tomar decisõese a fornecer informações num formato interativo e orientado. Algumas destas ferramentas são Análise multidimensional, que consiste na visualização de vários atributos relevantes, agregar dados, e realizar calculos avançados, com objetivo de criar formulas, realizar analises, comparações etc...

**Q29** #Data_warehousing, o que é e para que serve ?

	Data warehousing é uma abordagem de armazenamento e gerenciamento de dados. A carateristica principal da data warehousing consiste em organizar os dados e armazena-los de maneira otimizada de tal forma que permite consultas rápidas e eficientes.

**Q30** Quais os problemas de #Data_warehousing  ?

	Alguns dos problemas de data warehousing passam pela complexidade de implementação e de modelagem, o volume dos dados, ou seja, devem ser realizados estudos para prever que tipo de dados e qual o tamanho deles para evitar problemas futuros.

**Q31** Indique tipos de #Datamining.

	Data mining é uma tecnica que envolve a descoberta de padrões. Existem alguns tipos de data mining, sendo os mais conhecidos os métodos de regressão, que consiste para prever valores numéricos continuos com base em relações na base de dados, associação, que consiste em encontrar relações e padrões frequentes entre os dados num conjunto de transações e agrupamento que tem como objetivo a identificação e agrupamento de dados semelhantes na base de dados com base na similaridade ou dissimilaridade. 
	
**Q32** O que são #features e #targets numa aplicação de #datamining ?

	Features são variaveis de independentes que são utilizadas para dar valores a um determinado tipo de datamining. Elas representam informações relevantes da base de dados que influenciam os resultados finais de uma data mining.
	Targets são variaveis que dependem de alguma coisa, são aquelas que uma aplicação de datamining tenta prever. Estas represeantam resultados os resultados esperados.

**Q33** Como verificar de que maneira é feito o registo de informação em #Data_warehousing e se é síncrona ou assíncrona ?

