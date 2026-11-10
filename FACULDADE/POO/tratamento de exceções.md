# Mecanismo de exceções
- Serve para tratar erros ocorridos enquanto o código roda, de modo que o sistema continua funcionando;
- Exemplo: se você adicionar, no SIGAA, para upload, um arquivo maior que o esperado, o SIGAA gera um erro e continua a funcionar.
- Exceções são objetos da classe *Exception*;
	- `java.lang.Throwable`
		`java.lang.Exception`
			`// os tipos de exceção...` 
- Podemos criar nossas próprias exceções, herdadas (filhas) de *Exception*.

# Tipos de exceções: 
- Verificadas (checked):
	- O compilador já verifica no código fonte e sabe que uma exceção deve ser capturada;
	- O tratamento é obrigatório;
		- Pode ser feito com a estrutura *try-catch-finally* e com a cláusula *throws*.
	- Exemplos: `FileNotFoundException`.
- Não verificadas (unchecked):
	- Tipo RuntimeException;
	- O compilador Java não verifica o código-fonte para determinar se a exceção está sendo capturada;
	- Tratamento opcional;
	- Exemplo: `ArrayIndexOutOfBoundsException`.
- Para criar exceções, usa-se `@overrride` / uma classe filha de *Exception* e se define a nova exceção;

# Tratamento de exceções:
- *Try*: o código que tentará ser executado;
- *Catch*: pegará um erro que poderá vir do código em *Try*, com o errro especificado em tal *Catch*;
- *Finally*: última ação, sempre será feita, independente de erro ou não - mesmo que haja *return* em algum lugar, o *Finally*continuará sendo executado;
- *Throws*: dispara a exceção, para que quem tenha chamado a função com possível erro trate-o (como uma função que, quando chamada, delega o tratamento do erro para a main);
- *Throw*: lança uma exceção especificamente em um lugar do código;
- Para ser generalista na exceção disparada, coloca-se toda a classe *Exception*.