- toda imagem pode ser interpretada como arrays: fazemos matrizes;
- cada cor primária tem 8 bits, 256 variáveis;
- dividimos o arquivo em um cabeçalho, para mandar a interpretação de como ser lido ao programa, e no arquivo propriamente dito;
- em bmp, só usamos positivos, então, unsigned char (sem sinal);
- separa-se o cabeçalho e a imagem em arrays diferentes;
- 

SINTAXE:
- fopen("nomedoarquivo.bmp", "comoabrir")