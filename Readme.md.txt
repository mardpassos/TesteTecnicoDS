
a. Como foi a definição da sua estratégia de
modelagem?
b. Como foi definida a função de custo utilizada?

Primeiramente efetuei a importação da biblioteca pandas, a seguir fiz a leitura do arquivo para explorar os dados.

Segundo ao ver a tabela traz 13 colunas, somente uma não é numérica (type), as demais colunas trazem dados fisico-químicos dos vinhos. 
A ultima coluna nos traz a classificação do vinho e não tem nenhum valor faltante.

Dentre os valores referente a qualidade temos a nota mínima que é de 3, e a máxima que é de 9.
Realizei a correlação entre as colunas variáveis e a coluna qualidade, que é o target.
Não tive muito êxito nesta correlação.

Usei gráficos para analisar melhores resultados, usando a biblioteca matplotlib para isso precisei importá-las também.
No resultado a maior parte dos vinhos estão classificados entre 5 e 6.

c. Qual foi o critério utilizado na seleção do modelo
final?
d. Qual foi o critério utilizado para validação do
modelo? Por que escolheu utilizar este método?

O critério selecionado foi o algorítmo de árvore de decisão, usando a biblioteca Scikt-Learn, foi necessário importá-las também.

Comecei a preparar os dados para serem aplicados ao processo de classificação, com intuito de prever a 
qualidade dos vinhos através das outras variáveis. Primeiro separei as colunas entre varáveis (x) e 
coluna de qualidade (y). Desta forma consegui a base de calculos para a classificação.
As tabelas foram divididas em duas, x com 11 variáveis e y como principal foco.
Usei o metodo train_test_split para separar os dados, test_size para definir o percentual e o random_state para uma versão
randomica da divisão dos dados.

Em seguida foi criado um modelo classificador e max_leaf_nodes define a quantidade de nós na árvore de decisão.

Um teste usando x_test classifica a qualidade dos vinhos analistando as variáveis recebidas e em formato de numpy.ndarray o 
resultado foi armazenado em predictions.

e. Quais evidências você possui de que seu modelo é
suficientemente bom?

Para medir o percentual de acerto do modelo foi usado o accuracy_score, quanto mais próximo de 1, melhor o desempenho.
E o resultado foi de 0.5344908493664946.

