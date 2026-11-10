# Classes abstratas:
- São classes que não podem ser instanciadas, servem como base para suas classes-filhas;
- Representa uma **forma de garantir herança total**: somente subclasses não abstratas são instanciadas, nunca a superclasse abstrata;
- Usamos o tipo *abstract* para especificar que a nossa classe é abstrata;
	- Exemplo: `public abstract class Veiculo {}`;
- Os filhos continuam usando *extends* com a classe abstrata;
- Podem ter construtores e métodos, para que todas as filhas os herdem;
- Pode-se instanciar uma superclasse como nova subclasse:
	- Exemplo: `Personagem p = new Mago("Gandalf", 100.9f);`
	- Vantagens: 
		- Pode ser colocado em estruturas de dados facilmente;
		- Aceita a troca de subclasses desse objeto (o `Personagem p` pode ser transformado em um `new Guerreiro`);
- Também há métodos abstratos os quais devem ser aplicados em todos os filhos;
	- Métodos abstratos não podem ser usados pela classe-mãe;
	- Podem ser somente assinados, ou seja, só escritos, sem implementação;
	- Para utilizar nas filhas, é só reimplementar sem o *abstract* (override opcional);
	- O uso de métodos abstratos depende do contexto em que se implementa;
# Polimorfismo:
- Significa "muitas formas", permite ao desenvolvedor **usar o mesmo elemento de várias formas diferentes, com comportamentos diferentes**;
- Polimofismo estático (sobrecarga): ocorre quando há uma função com muitas formas minimamente diferentes, a mesma classe, com a mesma assinartura, é implementada muitas vezes;
	- Pode-se fazer **sobrecarga de construtores**;
- Polimorfismo dinâmico: acontece somente na herança, a subclasse sobrepôe o método original.
- Sobrescrita: 
	- O retorno deve ser o mesmo, o nível de acesso não pode ser restrito;
	- Usando *final* ou *private*, proíbe-se a sobrescrita, então, bloqueia-se o polimorfismo;
### Notas:
- Em um array de classe-mães, pode-se estanciar filhos;