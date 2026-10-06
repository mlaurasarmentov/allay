# Recursão:
- Problemas não computáveis: para || loop;
- Ciclo para resolução de um problema: uma função que chama a si mesma;
- Recursividade falha em uma pilha: stack overflow;
- A recursão é usada até um caso base ser alcançado;
	- Primeiro, define-se o caso base, depois, o caso recursivo;
	- Exemplo básico: fatorial;
- Copiar tabela dos slides!;
- Varags: função que usa parâmetros variados (arg: parâmetro, v: variado);
	- Permite a criação flexível de métodos;
	- Internamente, é um array;

# For each:

- Comando especial para fazer um laço *for*;
- Usado para percorrer uma estrutura de dados (coleções, vetores, arrays);
- Ideal quando não se precisa do índice do elemento;
	- `for (tipo de *elemento* (ex.: int i) : nome da coleção (ex.: números)){
	- `bloco de código }` 

# Arquivos:

- Permitem a persistência de dados - armazenamento de dados mesmo após o fim de um programa (ou seja, descobrir uma forma de salvar dados!);
- Evita a perda de informaçẽos;
- Normalmente, usamos bancos de dados para construir essa persistência;
- Bancos SQL: pastas -> arquivos -> tabelas -> registros;
	- Hierárquico: todas as entidades são relacionadas - banco relacional;
- Bancos noSQL: documental, grafos, chave-valor, vetorial...;
	- Usado para dados que não são exatamente uniformes, não têm a mesma estrutura;
- JDBC: conecta código à plataforma de dados;
- Leitura e escrita de arquivos: 
	- Leitura com Scanner - adiciona-se a classe File;
	- `File arquivo = *new* File("daddos.txt");`
	- `Scanner leitor = *new* Scanner(arquivo);`