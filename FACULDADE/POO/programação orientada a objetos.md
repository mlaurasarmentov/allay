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
	- Funciona por acesso indireto, para não corromper o dado - permite acesso controlado, para segurança, para organização etc.;
	- Esconde métricas e detalhes internos que não precisam ser acessados por entidades externas;
	- "Para uma abstração dar certo, sua implementação deve ser *encapsulada*".
- Herança: permite que um objeto ganhe métodos e características de outros objetos - ganham uma relação hierárquica entre si:
	- Classe mãe: super classe;
	- Relação de "é um".
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
- Métodos construtores: métodos base de alocação na memória;
	- Podem definir e iniciar atributos / métodos diferentes dos padrões JAVA (0 em int, por exemplo);
	- Quando se define um construtor, o padrão desaparece - precisa-se criá-lo explicitamente.
- Métodos destrutores: são responsáveis por liberar recursos usados;
	- Impedem vazamento de memória e crash;
	- Em JAVA, a própria JVM faz esse processo de modo automático.

## Palavras reservadas:
- Modificadores de acesso:
	- Public: pode ser usado por qualquer outra classe;
	- Private: permite visibilidade apenas da própria classe;
		- Em encapsulamento, faz-se o acesso por outros métodos, dentro da mesma classe (comumente, *get* e *set*);
	- Default: nível de pacote (em JAVA, seria pasta), permite visibilidade dentro do próprio pacote (não exige escrita explícita);
	- Protected: é como o Default, mas permite visibilidade global através de herança.
- *This*: faz referência ao objeto corrente, isto é, ao objeto usado no momento;
	- Ou seja, pega o atributo /  método com tal nome, em vez de, por exemplo, um parâmetro passado;
	- `this.ladoA = ladoA;
	  `this ladoB = ladoB;
- *Static*: aqui, é usado para diferenciar escopo de classe e escopo de instância;

## Composição / Delegação:
- A capacidade de se criar várias classes, usando classes que já existem;
- Classes podem ter outras classes como parâmetros em seus atributos;
- Usado para aproveitar código - é uma relação de "tem um".

## Herança:
- A principal ferramenta de reuso em POO -> novas classes são criadas a partir de classes inexistentes;
- Reutiliza todos os atributos e métodos não privados e pode adicionar novos recursos, separados da classe de origem;
- 

### Anotações gerais:
- No JAVA, há uma classe `LocalDate`, que guarda uma data específica instanciada;
	- `nascimento = new LocalDate(...);`
- Qualquer objeto pode vir com `null`, já que não é primitivo;
- É boa prática sempre ter um id para seu objeto, como identificador;