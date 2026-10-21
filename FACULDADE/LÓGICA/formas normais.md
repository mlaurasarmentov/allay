# Conceitos:

- Veremos sobre a transformação de fórmulas em fórmulas semanticamente equivalentes - obtenção de fórmulas com formas especiais, mais fáceis de determinar;
- Fórmulas normais usam somente ~ (negação), ^ (conjunção) e ∨ (disjunção);
- Literal: é um símbolo proposicional / a negação de um proposicional (p, ~p);
- Formas normais se dividem nos seguintes tipos:
	- Formas normais negativas: ~ ocorre apenas em literais;
		- Algoritmo: 
		- bicondicionais -> condicionais -> de Morgan -> dupla negação -> distributivas.
	- Formas normais conjuntivas: conjunção de disjunção de literais: (~p∨q) ^ (q∨p);
	- Formas normais disjuntivas: disjunção de conjunção de literais: (r^s) ∨ (s^~r);
		- Algoritmo:
		- fazer tabela-verdade -> pegar somente os finais V -> se a proposição for V, adiciona na conjunção sem mudança, se for F, adiciona a sua negação na conjunção -> liga as conjunções com disjunções.
