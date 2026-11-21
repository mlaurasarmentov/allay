# Como o programa define se está pronto?
- Agentes rodam em loop de ler, programar, verificar e decidir seu próximo passo - se houver algum erro no caminho (erro na compilação, por exemplo), ele o corrige e volta ao loop original;
- Ele decide se o programa está pronto lendo seu próprio código, mas é o usuário quem testa o programa feito e repassa possíveis bugs (o usuário, assim, vira o loop de verificação necessário);
- Com isso em mente, checagens devem medir o programa e trazer uma resposta no universo de duas possibilidades: sim e não - ou está correto, ou precisa de mudanças;
	- Para os agentes, suas checagens são melhores sendo objetivas e claras - sempre será melhor uma checagem prática, como um exemplo numérico, que um adjetivo, ou seja, estados que podem ser conferidos pela máquina;
	- Porém, nem toda checagem pode ser numérica!
- 