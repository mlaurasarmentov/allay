**CONVERSÃO:**
- Operadores relacionais (comparadores, retornam 0 e 1);
- Operadores lógicos (&&, ||, ! - "e", "ou" e "não") e curto-circuito;
	- Precedência = conjunção;
	- O interpretador considera curto-circuito como precedência primária!;

- Conversão de tipos:
	- Implícito - Promoção: automático, ocorre quando os tipos são compatíveis, sempre em ordem crescente (do tipo menor para ou maior; de tipos iguais para um igual ou maior);
	- Explícito - Casting: manual, ocorre com tipos não compatíveis, de um tipo maior para um tipo menor;
	- Há comandos para conversão numérico -> string e string -> numérico: usam-se funções do tipo.

- Cuidado com strings! Melhor criar várias Strings em vez de somente mudar seus valores, para se saber quando as Strings serão eliminadas;


**ENTRADA E SAÍDA DE DADOS:**
- String é um objeto facilitado, a fim de ser usado como variável;
- Objeto scanner: classe com exportação (java.util.Scanner);
- Com scanner, lemos os dados de qualquer tipo padrão;
	- Scanner scanner = new Scanner (System.in); *Instanciar: declarar um objeto a partir de uma classe - criar, iniciar e projetar*
	- "new": novo objeto de tal classe;
	- "()": nos parêntesis, colocamos os parâmetros (no caso, de onde virão as informações do scanner);
- Input mismatch: erro / confusão de entrada (cuidado!);
- .next e .nextLine: o primeiro pega palavra por palavra, enquanto o segundo lê tudo, até achar um enter;
- Caixa de diálogo (javax.swing.JOptionPane): só lê String, abre uma janelinha.

