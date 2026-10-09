# Revisão:

- Front:
	- Interação de usuário;
	- Visualização;
	- Design;
	- Requisições;
	- Hospedado na web, mas usa o poder de processamento local;
	- Front -> Autenticação -> API.
- Back:
	- Deixa a aplicação segura e a faz funcionar;

# Sobre memória:

- Em vez de usar memória RAM, você usa uma memória mais lenta, mas maior;
- Durabilidade, 
- Aumenta a escalabilidade;
- Pode ser usado por várias máquinas ao mesmo tempo;
- Por que não arquivos?
	- Salva, mas não escala;
	- Busca lenta: precisa ler o arquivo inteiro;
	- Dados repetidos;
	- Não permite escrita concomitante - apaga uma das requisições;

# Que é um banco de dados?

- Guarda, *organiza* e entrega dados rápido, sempre que é requisitado;
- Fácil de encontrar informações;
- Ajuda a mexer nos dados e a controlar quem acessa (princípio do mínimo acesso);
- Faz autenticação;
## Dados e bancos:
- Dados estruturados: formato fixo (linhas e colunas);
- Dados semiestruturados: tem estrutura, mas cada registro pode ter campos diferentes (pode ter tipos diferentes por registo);
- Dados não estruturados: sem organização e sem formato definido - o banco guarda, mas não entende o conteúdo;
- Banco relacional:
	- Tabelas: cada tabela tem nome único, linhas e colunas;
	- Dados relacionados: tabelas se conectam por chaves - PK (chave primária) identifica cada registros, FK (chave estrangeira) aponta parq o PK de outra tabela;
	- Usa operações básicas de manipulação por queries;
		- Hard delete: exclusão total de dados;
		- Soft delete: dados recebem uma flag de "apagado", mas os dados continuam.
	- Faz o processamento de consultas;
	- Propriedades:
		- Atomicidade: ou a ação passa, ou ela é apagada;
		- Consistência;
		- Isolamento: faz processos separados de forma isolada e, depois, junta-os;
		- Durabilidade: garante que as informações de uma transação, depois de confirmada, continue salva;
- Índice: normalmente é sequencial, permite acesso por busca binária, adicionando uma coluna a mais;
	- Mais rápido que a busca um por um;
	- Aumenta muito o peso do banco de dados;
	- Raiz -> Nível 2 -> Folha -> Tabela.
- UUID (PK): um ID que nunca muda, serve para guardar sempre o endereço de um registro - é o verdadeiro campo de identificação (quando deletado, normalmente, só fica "invisível" e foda-se (palavras de João));
- SQL: é declarativo, é a linguagem do banco;
	- DDL: define estrutura;
	- DML: mexe nos dados;
	- DQL: consulta os dados;
	- DCL: controla acesso.
- Tipos de bancos de dados:
	- 

- Docker e containeres: