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

Declarações com **let** são escritas da mesma forma que declarações com **var**. A principal diferença, no entanto, não é a sintaxe, mas a semântica. Propriedades como: block-scoping, sem re-declarations, shadowing permitem que alguns dos bugs provenientes do uso do **var** sejam evitados.

`let hello = "Hello!";`
<h4>Declarando com const</h4>

Declarações com **const** são outra forma de declarar variáveis. Elas são parecidas com declarações com **let**, mas seus valores não podem ser alterados depois de definidos.

`const numLivesForCat = 9;`

<h3>Operadores relacionais e lógicos</h3>
<h4>Operadores relacionais</h4>

Operadores relacionais testam ou definem o tipo de relação entre duas entidades. Estes operadores retornam um valor booleano, i.e., true/false.

Assuma que o valor de A é 10 e de B é 20.

| Operador | Descrição | Exemplo | 
| :---: | :---: | :---: |
| > | maior que | (A > B) é false |
| < | menor que | (A < B) é true |
| >= | maior ou igual que | (A >= B) é false |
| <= | menor ou igual que | (A <= B) é true|
| == | igual | (A == B) é false|
| != | diferente | (A != B) é true|

<h4>Operadores lógicos</h4>

Operadores lógicos são utilizados para combinar duas ou mais condições. Estes operadores também retornam um valor booleano.

Assuma que o valor de A é 10 e de B é 20.

| Operador | Descrição | Exemplo | 
| :---: | :---: | :---: |
| && (E) | o operador retorna true somente se todas as expressões forem verdadeiras | (A > 10 && B > 10) é false |
| \|\| (OU) | o operador retorna true se pelo menos uma expressão for verdadeira | (A > 10 \|\| B > 10) é true |
| ! (NÃO) | o operador retorna o inverso do resultado da expressão | !(A > 10) é true |

<h3>Operadores aritméticos</h3>

Assuma que os valores das variáveis **a** e **b** são 10 e 5 respectivamente.

| Operador | Descrição | Exemplo | 
| :---: | :---: | :---: |
| + (Adição) | retorna a soma dos operandos | a + b é 15 |
| - (Subtração) | retorna a diferença dos operandos | a - b é 5 |
| * (Multiplicação) | retorna o produto dos operandos | a * b é 50 |
| / (Divisão) | retorna o quociente da divisão | a / b é 2 |
| % (Resto) | retorna o resto da divisão | a % b é 0 |
| ++ (Incremento) | aumenta o valor da variável em um | a++ é 11 |
| -- (Decremento) | diminui o valor da variável em um | a-- é 9 |

<h3>Estruturas de controle condicional</h3>

Estruturas condicionais requerem que o programador especifique uma ou mais condições a serem avaliadas ou testadas pelo programa, juntamente com uma ação ou ações que serão executadas caso a condição seja declarada verdadeira, e opcionalmente, outras ações que serão executadas caso a condiação seja declarada falsa.

<h4>if</h4>

O controle **if** verifica uma expressão antes de um bloco de código ser executado.

```
if(expressao) {
   // ação(ões) será(ão) executada(s) se a expressão for verdadeira  
} 
```

Se a expressão for verdadeira, o bloco de código dentro do if será executado. Se for falsa, a primeira linha de código após o if será executada. 

<h5>Exemplo</h5>

```
var  num:number = 5
if (num > 0) { 
   console.log("Número positivo") 
}

\\Número positivo
```

<h4>if...else</h4>

Um **if** pode ser acompanhado por um bloco opcional **else**. O bloco **else** será executado se a expressão testada pelo **if** for falsa.

```
if(expressao) {  
   // ação(ões) será(ão) executada(s) se a expressão for verdadeira
} else {
   // ação(ões) será(ão) executada(s) se a expressão for falsa  
}
```

<h5>Exemplo</h5>

```
var num:number = 12; 
if (num % 2==0) { 
   console.log("Par"); 
} else {
   console.log("Ímpar"); 
}

//Ímpar
```

<h4>else...if</h4>

O controle **else...if** é recomendado para testes de múltiplas condições.

```
if (expressao1) { 
   //ações caso a expressao1 seja verdadeira 
} else if (expressao2) { 
   //ações caso a expressao2 seja verdadeira 
} else { 
   //ações caso ambas as expressao1 e expressao2 sejam falsas 
}
```

<h5>Exemplo</h5>

```
var num:number = 2 
if(num > 0) { 
   console.log(num+" é positivo") 
} else if(num < 0) { 
   console.log(num+" é negativo") 
} else { 
   console.log(num+" é nem positivo, nem negativo") 
}

//2 é positivo
```

<h4>switch</h4>

O controle **switch** avalia uma expressão, combina o valor da expressão com uma cláusula case e executa a ação associada ao caso.

```
switch(expressao) { 
   case expressao1: { 
      //ações; 
      break; 
   } 
   case expressao2: { 
      //ações; 
      break; 
   } 
   default: { 
      //ações; 
      break; 
   } 
}
```

<h5>Exemplo</h5>

```
var nota:string = "A"; 
switch(grade) { 
   case "A": { 
      console.log("Excelente"); 
      break; 
   } 
   case "B": { 
      console.log("Bom"); 
      break; 
   } 
   case "C": {
      console.log("Regular"); 
      break;    
   } 
   case "D": { 
      console.log("Ruim"); 
      break; 
   }  
   default: { 
      console.log("Opção Inválida"); 
      break;              
   } 
}

//Excelente
```

<h3>Estruturas de repetição</h3>

Uma estrutura de repetição permite a execução de uma ação ou bloco de ações múltiplas vezes. TypeScript fornece vários tipos de estruturas de repetição.

<h4>Repetições definidas</h4>

Repetições cuja quantidade de interações são determinadas/fixas. **for** é um tipo de implementação dessa categoria.

<h5>for</h5>

A estrutura **for** executa um bloco de código por um número específico de vezes.

```
for (valor_inicial_contador; condicao_final; passo) {
   //ações 
}
```

A estrutura usa uma variável contadora para registrar as interações. O loop inicia a interação definindo o valor inicial do contador e executa o bloco de código enquanto o valor do contador satisfazer a condicao_final. O passo altera o valor do contador após cada interação.

<h6>Exemplo</h6>

```
var num:number = 5; 
var i:number; 
var fatorial = 1; 

for(i = num;i >= 1;i--) {
   fatorial *= i;
}
console.log(fatorial)

//120
```

<h4>Repetições indefinidas</h4>

Repetições indefinidas são utilizadas quando a quantidade de interações é indeterminada ou desconhecida. Podem ser utilizada as estruturas **while** e **do...while**.

<h5>while</h5>

A estrutura **while** executa as instruções toda vez que a condição especificada for verdadeira. Em outras palavras, a estrutura verifica a condição antes de executar o bloco de código.

```
while(condicao) { 
   // ações caso a condição seja verdadeira 
}
```

<h6>Exemplo</h6>

```
var num:number = 5; 
var fatorial:number = 1; 

while(num >=1) { 
   fatorial = fatorial * num; 
   num--; 
} 
console.log("O fatorial  é "+fatorial);

\\O fatorial é 120
```

<h5>do...while</h5>

A estrutura **do...while** é similar a do **while** exceto que essa não valida a condição na primeira vez que a repetição é realizada. No entanto, nas interações seguintes, a condição será validada. Em outras palavras, o bloco de código será executado, no mínimo, uma vez.

```
do {
   //ações 
} while(condicao)
```

<h6>Exemplo</h6>

```
var n:number = 10;
do { 
   console.log(n); 
   n--; 
} while(n>=0); 

\\10
\\9
\\8
\\7
\\6
\\5
\\4
\\3
\\2
\\1
\\0
```

<h3>Vetores, matrizes e strings</h3>
<h4>Vetor</h4>

TypeScrypt, assim como JavaScipt, permite trabalhar com vetores de valores. Vetores podem ser escritos de duas formas. Na primeira forma, declara-se o tipo do elemento seguido de **[ ]**:

`let list: number[] = [1, 2, 3];`

A segunda forma utiliza uma forma genérica de vetor, **Array<[tipo]>**:

`let list: Array<number> = [1, 2, 3];`
<h4>Matriz</h4>

Um vetor pode ter como valor uma referência a outro vetor. Esse tipo de vetor é chamado de vetor multidimensional. A forma mais simples desse tipo de vetor é um vetor bidimensional.

<h5>Declarando um vetor bidimensional</h5>

`var nome_vetor:tipo_dado[][]=[ [val1,val2,val3],[v1,v2,v3] ]`

<h5>Acessando um elemento de um vetor bidimensional</h5>

`nome_vetor[indice_vetor_inicial][indice_vetor_referenciado]`

<h5>Exemplo</h5>

```
var multi:number[][] = [[1,2,3],[23,24,25]]  
console.log(multi[0][0]) 
console.log(multi[0][1]) 
console.log(multi[0][2]) 
console.log(multi[1][0]) 
console.log(multi[1][1]) 
console.log(multi[1][2])

\\1
\\2
\\3
\\23
\\24
\\25
```

<h4>String</h4>

Como em outras linguagens, utilizamos o tipo **string** para referir-se a dados textuais. Assim como em JavaScript, TypeScript utiliza aspas duplas ( **"** ) ou aspas simples ( **'** ) para delimitar o valor da string.

```
let color: string = "blue";
color = 'red';
```
<h3>Funções</h3>

Assim como em JavaScipt, funções em TypeScipt podem ser criadas com ou sem nome (anônimas).

```
// Função com nome
function add(x, y) {
    return x + y;
}

// Função anônima
let myAdd = function(x, y) { return x+y; };
```
<h2>Sintaxe OO</h2>

Essencialmente, JavaScript usa funções para construir componentes reutilizáveis. No entanto, TypeScript é orientada a objetos, permitindo a criação de classes, interfaces, etc.
<h3>Classes</h3>

Uma classe encapsula dados para o objeto.

```
class nome_classe { 
   //corpo da classe 
}
```

A palavra-chave class é seguida pelo nome da classe. Regras de identificação devem ser consideradas ao nomear-se uma classe.

Uma classe pode conter:

* Atributos - Um atributo é qualquer variável declarada em uma classe. Atributos representam dados pertencentes a objetos.
* Construtores - Responsáveis por alocarem memória para os objetos da classe.
* Métodos - Os métodos representam ações que um objeto pode realizar.

<h4>Exemplo</h4>

```
class Car { 
   //atributo 
   engine:string; 
 
   //construtor 
   constructor(engine:string) { 
      this.engine = engine 
   }  

   //método 
   disp():void { 
      console.log("Engine is  :   "+this.engine) 
   } 
}
```
<h3>Objetos</h3>

Um **objeto** é uma instância de uma classe. Para criá-lo, use a palavra-chave **new** seguida pelo nome da classe.

```
var nome_objeto = new nome_classe([ argumentos ])
```

* A palavra-chave **new** é responsável pelo instanciamento.
* O lado direito da expressão invoca o construtor. Devem ser passados valores, caso o construtor tenha parâmetros.

<h4>Exemplo</h4>

`var obj = new Car("Engine 1")`

<h3>Atributos</h3>

Um atributo é qualquer variável declarada em uma classe. Eles representam dados pertencentes a objetos.

```
class Car { 
   //atributo 
   engine:string;
   
   ...
 }
```

Considerando a classe Car, declarada acima. Ela tem um atributo chamado engine. Atente-se ao fato de que a palavra-chave **var** não é utilizada para declarar um atributo.

<h4>Visibilidade</h4>

Uma classe pode controlar a visibilidade de seus membros, entre eles, seus atributos, para outras classes. Essa habilidade é denomidada Encapsulamento, um dos princípios OO.

<h5>public</h5>

Um componente público tem acessibilidade universal, ou seja, pode ser acessado por qualquer componente. Componentes de uma classe são, por padão, públicos.
<h5>private</h5>

Componentes privados são acessíveis, apenas, dentro da classe que os definem. Se um componente externo a classe tentar acessar um componente privado, o compilador lança um erro.
<h5>protected</h5>

Um componente protegido é acessível por componentes pertencentes a mesma classe dele ou a classes filhas.

<h5>Exemplo</h5>

```
class Encapsulate { 
   str:string = "hello" 
   private str2:string = "world" 
}
 
var obj = new Encapsulate() 
console.log(obj.str)     //acessível 
console.log(obj.str2)   //Erro de compilação, já que str2 é privado
```
<h4>Acessando um atributo</h4>

Um atributo de uma classe pode ser acessado atráves de um objeto. É utilizada a notação com o '.' (ponto) para acessar esses valores.

`obj.nome_atributo `
<h3>Métodos</h3>

Os métodos representam ações que um objeto pode realizar.

```
class Car { 
   ... 
 
   //método 
   disp():void { 
      console.log("Engine is  :   "+this.engine) 
   } 
 }
```

disp() é uma definição simples de uma função. Observe que a palavra-chave function não é utilizada aqui!

<h4>Acessando um método</h4>

O acesso a um método de uma classe, segue a sintaxe a seguir:

`obj.nome_funcao()`
<h3>Construtores</h3>

Um construtor é uma função especial de uma classe responsável por inicializar os atributos dela. TypeScript define um construtor pela palavra-chave constructor. Um construtor é uma função e, portanto, pode ter parâmetros.

```
class Car { 
   ... 
 
   //construtor 
   constructor(engine:string) { 
      this.engine = engine 
   }  

   ... 
}
```

A palavra-chave **this**, utilizada no exemplo acima, refere-se a instância atual da classe. No exemplo citado, o nome do parâmetro (engine) é o mesmo que o nome de um atributo da classe. Para evitar ambiguidade, o atributo é antecedido pela palavra-chave **this**.
<h3>Herança</h3>
<h3>Polimorfismo</h3>
<h3>Sobrecarga</h3>
<h3>Exceções</h3>
<h4>Categorias de exeções</h4>
<h4>Captura e lançamento de exceções</h4>
<h4>Criar novas exeções</h4>
<h2>Sintaxe Funcional</h2>
