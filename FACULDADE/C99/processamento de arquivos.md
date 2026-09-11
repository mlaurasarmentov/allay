processamento de entrada e de saída:troca de dados entre o computador e seus dispositivos periféricos;

operação de entrada: dados do dispositivo copiados na RAM (teclado, mouse);
operação de saída: dados da RAM copiados no dispositivo (tela, LED);

arquivo: qualquer dispositivo que pode ser entrada, saída;

modos de entrada:
- "r": leitura, só funciona com um arquivo pre-existente;
- "w": escrita, pode criar um arquivo, mas, se o arquivo for pre-existente, ele destrui-lo-á;
- "a": append, deixa adicionar informações no fim de um arquivo;

SINTAXE:
- redirecionamento de saída: ./programa > saída.txt
	- para append: ./programa >> programa.txt
- redirecionamento de entrada: ./programa < entrada.txt
- 
- fopen ("/caminho/para/arquivo.txt", "modo")
- fclose(FILE * stream)