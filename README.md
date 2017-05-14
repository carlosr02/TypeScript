# TypeScript
Carlos Romero Bacurau de Brito (carlosr02), 20141011110255
<h2>Resumo</h2>

* Propósito da linguagem: projetada para o desenvolvimento de aplicações de grande porte. Pode ser utilizada para desenvolver aplicações JavaScript para front-end e back-end (Node.js);
* Multiparadigma: scripting, orientada a objetos, estruturada, imperativa, funcional, genérica;
* Data de criação: 2012 por [Anders Hejlsberg](https://pt.wikipedia.org/wiki/Anders_Hejlsberg); e,
* Principal mantenedor: [Microsoft](https://www.microsoft.com/pt-br/).
<h2>Instalação e Uso</h2>
Proceda a uma das opções abaixo para instalar as ferramentas TypeScript:

* Execute o comando a seguir na linha de comando: `npm install -g typescript` ou
* Faça a instalação do plugin para o Visual Studio: [TypeScript for Visual Studio 2015](https://www.microsoft.com/en-us/download/details.aspx?id=48593)

Para compilar, execute o comando a seguir: `tsc [nome_arquivo].ts`
<h2>Sintaxe Básica</h2>
<h3>Variáveis e constantes</h3>

**let** e **const** são dois novos tipos de declaração de variáveis em JavaScript. **let** é semelhante a **var** em alguns aspectos, mas permite que o usuário evite algumas armadilhas recorrentes em JavaScipt. **const** é um acremento de **let** que previne reatribuição de valores a uma variável.
<h4>Declarando com let</h4>

Declarações com **let** são escritas da mesma forma que declarações com **var**. A principal diferença, no entanto, não é a sintaxe, mas a semântica. Propriedades como: block-scoping, re-declarations, shadowing permitem que alguns dos bugs provenientes do uso do **var** sejam evitados.

`let hello = "Hello!";`
<h4>Declarando com const</h4>

Declarações com **const** são outra forma de declarar variáveis. Elas são parecidas com declarações com **let**, mas seus valores não podem ser alterados depois de definidos.

`const numLivesForCat = 9;`

<h3>Operadores relacionais e lógicos</h3>
<h3>Operadores aritméticos</h3>
<h3>Estruturas de controle condicional</h3>
<h3>Estruturas de repetição</h3>
<h3>Vetores, matrizes e strings</h3>
<h4>Vetor</h4>

TypeScrypt, assim como JavaScipt, permite trabalhar com vetores de valores. Vetores podem ser escritos de duas formas. Na primeira forma, coloca-se o tipo do elemento seguido de **[]**:

`let list: number[] = [1, 2, 3];`

A segunda forma utiliza uma forma genérica de vetor, **Array<elemType>**:

`let list: Array<number> = [1, 2, 3];`
<h3>Funções</h3>

<h2>Sintaxe OO</h2>
<h2>Sintaxe Funcional</h2>
