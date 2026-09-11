
com ralf! :D

1. Conceitos básicos:
- Que é? = Vamos abstrair coisas! Mapear conceitos, objetos e comportamentos (ações e estados) da vida real para elementos de software;
- Vamos entender o código de outras pessoas!
	- Exemplo: blueprints com regras, vamos criar plantas e moldes. É sobre padronização.
- Classe: é a nossa planta/nosso molde. Regras que vamos seguir para fazer nosso objeto;
- O OBJETO É A INSTÂNCIA DE UMA CLASSE: para fazer um objeto, instanciaremos uma classe;
	- Programação e cópia: reutilização.
- Abstração:
	- UML: diagrama de classes.
	- Vamos pegar nossa classe e dividir em três faixas: 
		- Nome;
		- Métodos: comportamentos (são funções! ou seja, sempre tem parêntesis ());
		- Atributos: características.
	- Objetos podem ser reais (carro) ou abstratos (aula, consulta).
- Objeto como evolução da variável: guardam dados e comportamentos.

2. Classes:
- Estaremos lidando com Python!
- No python, declaramos objetos que vêm de classes, quando usamos variáveis.
- Estrutura:
	- class NOME:
			- def __init__(self, atributos...)
				- self.atributo1 = exatributo1
				- self.atributo2 = exatributo2
		- init = já estamos instanciando: método construtor, tem os dados obrigatórios para a classe e (normalmente) um self;
			- EXEMPLO: obj = minhaclasse()
		- self = cria-se um objeto próprio que segue a classe; assim, entre mil zumbis, eles não são ligados necessariamente (podem receber dano com vidas únicas, mesmo com mesmo valor);
		- lembre-se de chamar sua classe!
		- toda classe, no python, tem construtor;

3. Encapsulamento: 
- Cuidado ao usar pontos em atributos/métodos! 
- Por isso, há o encapsulamento: 
	- + é o valor público (no python: self.exemplo1 = );
	- Assim, # é o protected (no python: self._exemplo =);
	- - é o privado (no python: self.__exemplo =);
	- Métodos para retornar ou alterar atributos (usando o método indireto):
		- Getters e Setters.
		- Get: pega algo do objeto
		- Set: coloca algo no objeto, ajuda em alterações.

4. Herança:
- Classes que herdam atributos e comportamentos de uma classe principal, não necessariamente da mesma forma;
- Elas podem ter características centrais diferentes;
	- EXEMPLO: class SystemError (Exception) = a classe SystemError herda da classe Exception;
- As classes *não necessariamente* precisam estar uma dentro da outra;
- Overriding: esquecemos o método herdado para fazer um específico para a classe filha, ou seja, sobrescrevemos um processo;
- "super()" aproveita o método da mãe e adiciona algo.

5. Polimorfismo:
- Poli (múltipla) + morfo (forma);
	- EXEMPLO:
		- for alvo in alvos:
			- alvo.receber_dano(3)
			- // nesse exemplo, nós só mexemos com métodos comuns entre nossas classes! algo como ENTRE ANIMAIS: FAZEM SOM; CASCAVEL: ARG1; COELHO: ARG1, ARG2.
- Overloading: dois métodos com mesmo nome; dependendo dos argumentos, escolhe-se um deles (impossível no python: chamamos o método abaixo de Overloading, simplesmente para o caso do python);
- Usamos mais argumentos ou argumentos diferentes para o polimorfismo;
- Colocamos if/elses para os nossos argumentos;
	- EXEMPLO: def processar(self, valor, parcelas = None, chavepix = None):
		- if parcelas: ...
		- elif chavepix: ...
		- else: ...
- Por fim, um mesmo método teve duas formas: uma para quando temos o argumento parcelas e outra para quando temos o argumento chavepix.
