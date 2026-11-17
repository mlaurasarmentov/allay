# Interface:
- Um mediador entre usuário e código -  é algo que provém serviço;
	- `public interface <nome>`;
- Estabelece um *contrato* entre classes, não são instanciadas;
- *Contrato*: sequência de métodos que devem ser implementados pela classe que usa tal interface;
- Funciona como classes abstratas, mas sem método implementado;
- Pode, também, usar somente as assinaturas de métodos abstratos (as classes quem implementam os métodos);
- Pode-se estabelecer uma implementação padrão
- Uma interface pode extender outra interface;
- Toda classe pode implementar diversas interfaces - é uma maneira de driblar a limitação de herança única em classes;
- Exemplo: uma `interface CRUD` pode ter vários métodos, como `criar()`, `deletar()` `ler()` e `atualizar()`;
	- Tudo que interage com `CRUD` precisa fazer tais métodos;
	- Para usar: `public class <classe> implements <interface> {}`
- Diferenças: classes abstratas recebem atributos, não necessariamente há uma relação de herança entre classes que implementam uma interface;

## Java Collections:
- Fornece uma série de coleções (funcionam como *estruturas de dados*) ao programador;
	- *Estruturas de dados*: organizam de modos diferentes dados desejados;
	- Essas coleções são feitas para ultrapassar algumas limitações dos arrays (tamanho definido, dificuldade de deleção...);
- Os três grandes tipos são:
	- Listas;
	- Conjuntos;
	- Mapas;
- *List*: divide-se em duas implementações - ArrayList, LinkedList e Vector;
	- Homogênea e ordenada;
	- ArrayList: é um array que se parece com uma lista dinâmica - a JVM cuida da memória para o programador;
		- `ArrayList<TIPO> nome = new ArrayList<TIPO> ();`
		- `List<TIPO> nome = new ArrayList<TIPO> ();`
	- LinkedList: cada elemento tem uma referência para o próximo e para o anterior - não consegue pegar um elemento específico com pouco gasto;
	- Vector: parece-se com o ArrayList, apresenta inserção e deleção;
