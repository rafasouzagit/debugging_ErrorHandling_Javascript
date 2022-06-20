# Debbugging e Error Handling

<h2>Error do ECMAScript</h2>
<p>É um erro  que ocorre em tempo de execução, quando por exeplo você esquece um ponto e virgula.</p>
<p>É composto por:</p>
<p>- Mensagem</p>
<p>- Nome</p>
<p>- Linha</p>
<p>- Call Stack: pilha de chamadas</p>
<br>
<h2>DOMException</h2>
<p>É uma exceção(erro) no documento relacionado a página da Web, como por exemplo colocar um caractere errado na hora de consumir um dado.</p>
<p>São erros referentes a estrutura da sua árvore de elementos dentro de uma página da Web.</p>
<br>
<h2>Throw, Try Catch e Finally</h2>
<br>
<p>Throw: trata o "retorno" como um erro, por exemplo quando em uma função quero checar se o valor de uma string é inválido:</p>
<br>
<p>No return fica :</p>
<p>if (!string) return "String inválida";</p>
<br>
<p>Ele irá retornar a "String Invalida"</p>
<br>
<p>No Throw fica: </p>
<p>if (!string) throw "String inválida";</p>
<p>Irá retornar o erro Uncaught: String inválida</p>
<br>
<h2>Try...Catch</h2>
<p>O try verifica um bloco de código e se dá erro ele vai pro catch</p>
<p>No catch voce manipula o erro da maneira que preferir.</p>
<br>
<h2>Finally</h2>
<p>Instrução que vai ser chamada independente de ter um erro ou não</p>
<br>
<h2>Objeto Error</h2>
<p>new Error(message,fileName, lineNumber</p>
<p>//todos os parametros são opcionais o mais usado é o message por ser aceito por todos os navegadores</p>
<p>const MeuErro = new Error('Mensagem Inválida");</p>
<p> throw Meu erro;</p>
<br>
<p>O erro pode ter um nome após ser criado:</p>
<p>MeuErro.name = 'InvalidMessage';</p>
<br>
<h3>Atividade: validação de erros por tipo</h3>
<p>O objetivo é que a função receba um array e retorne ele caso o seu tamanho corresponda ao número enviado como parâmetro na função. Caso contrário, um erro será lançado.

<p>Crie uma função que recebe um array e um número</p>
<p>Realize as seguintes validações</p>
<p>-Se os parâmetros não forem enviados, lance um erro do tipo ReferenceError</p>
<p>-Se o array não for do tipo 'object', lance um erro do tipo TypeError</p>
<p>-Se o número não for do tipo 'number', lance um erro do tipo TypeError</p>
<p>-Se o tamanho do array for diferente do número enviado como parâmetro, lance um erro do tipo RangeError</p>
<p>Utilize a declaração try...catch</p>
<p>Filtre as chamadas de catch por cada tipo de erro utilizando o operador instanceof</p>