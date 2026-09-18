- Inteligência artificial -> Machine learning -> Deep learning;
- Paradigma tradicional: input e regras claras - o computador passa o output;
- Machine learning: dados e respostas - o computador descobre as regras;
	- Usamos experiência (dados passados) para resolver uma tarefa e calculamos como foi o desempenho;

- **Tipos de aprendizagem:**
	- Supervisionado: cada exemplo tem resposta;
		- Tipos: 
			- Classificação: separar classes de dados, não costuma usar números reais;
			- Regressão: números reais, descrição do comportamento dos dados;
			- Linear: usam dados linearmente separados (retas!);
			- Não-linear: usam dados que não conseguem usar retas em sua separação (curvas, normalmente em problemas maiores);
	- Não-supervisionado: sem respostas -> deve-se encontrar um padrão;
	- Por reforço: tentativa, erro e recompensa (pontos);

- **Perceptron:**
	- Algoritmo classificador binário: f(x) = h(xw + b);
		- Em que:
		- x são features do dataset (estabelecidas antes);
		- w são os pesos (mudados de acordo com as tentativas);
		- b são os vieses;
		- função h: step, aproxima valores;
	- Funciona em passos:
		- Inicialização de pesos;
		- Para cada exemplo:
			- Calcula a saída;
			- Compara e atualiza os pesos de acordo com o output desejado;
			- Incrementa o tempo;
	- Nota: a função h não é derivável, de modo que, para algoritmos modernos, não é usada;

- **Árvores de decisão:**
	- Muito usado para problemas clássicos de machine learning;
	- Procura uma função de divisão para separar os dados colocados em grupos, de forma não-linear;
	- Números menores sempre à esquerda;
	- Ele procura por regras ótimas para o dataset apresentado;
	- Pode-se controlar a profundidade e o número de árvores;

- **Overfitting e underfitting:**
	- Overfitting: a máquina se acostuma somente aos exemplos dados -> falta generalização (geralmente em modelos de alta variância);
	- Underfitting: não diferencia bem, pois não se acostuma bem aos exemplos dados -> muito generalizado (caso do perception em dados muito complexos);

- 