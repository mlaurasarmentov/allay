# Programação Orientada a Objetos:

- Usa dados locais / pertencentes a objetos - vários procedimentos podem ser associados a eles;
	- Cada objeto tem um conjunto de estados;
	- Assim, comumente, não se usam dados globais.
- Usa alguns conceitos básicos para o seu manuseio - os pilares de POO;

## Pilares de POO:

- Abstração: a representação de objetos, remete a um objeto, é uma generalização:
	- É o processo de isolar ou de simplificar um conceito;
	- Uma visualização ou representação de uma entidade que inclui somente os atributos de importância em um contexto particular;
	- Esconder detalhes de implementação, expondo apenas uma interface simples.
- Encapsulamento: é o processo de esconder os detalhes não necessários para um objeto:
	- Explica como um atributo deve ser acessado, para não quebrar o programa;
	- Funciona por acesso indireto, para não corromper o dado;
	- "Para uma abstração dar certo, sua implementação deve ser *encapsulada*".
- Herança: permite que um objeto ganhe métodos e características de outros objetos - ganham uma relação hierárquica entre si:
	- Classe mãe: super classe.
- Polimorfismo: diferentes formas para um mesmo método - a mesma função, dependendo do contexto, pode se manifestar de modos diferentes;
- Classe: comumente, cria-se com letra maiúscula:
	- Propriedades (estados): características gerais de objetos dessa classe:
	- Métodos (comportamentos / operações): ações que podem ser realizadas com os objetos dessa classe;
	- Define atributos e métodos, é aquilo codificado, base para objeto - é um molde / um modelo para o objeto;
	- Começa com qualificador (public, ou private);
	- Declaração: `Classe nomeClasse = new Construtor`.
		- O construtor define parâmetros, caso desejado.
- Objeto: é a abstração de algo do mundo real, colocada na memória do computador e, assim, cabível de processamentos:
	- É criado a partir de classe (pelo comando *new*) - baseia-se no que já foi definido;
	- É instanciado na memória e tem seus dados únicos guardados;
	- Comunicação entre objetos: usam mensagens para mandar requisições a diferentes objetos;

- Modificadores de acesso:
	- Public: pode ser usado por qualquer outra classe;
	- Private: permite visibilidade apenas da própria classe;
	- Default: nível de pacote (em JAVA, seria pasta), permite visibilidade dentro do próprio pacote (não exige escrita explícita);
	- Protected: é como o Default, mas permite visibilidade global através de herança.
- Construtores: métodos base de alocação na memória;
	- Podem definir e iniciar atributos / métodos diferentes dos padrões JAVA (0 em int, por exemplo);
	- Quando se define um construtor, o padrão desaparece - precisa-se criá-lo explicitamente.
- Destrutores: são responsáveis por liberar recursos usados;
	- Impedem vazamento de memória e crash;
	- Em JAVA, a própria JVM faz esse processo de modo automático.