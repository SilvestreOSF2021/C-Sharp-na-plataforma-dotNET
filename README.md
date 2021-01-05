
[_Documentação do C#_](https://docs.microsoft.com/pt-br/dotnet/csharp/) Saiba como escrever qualquer aplicativo usando a **Linguagem de programação C# na plataforma .NET.**

[Tipos (Guia de Programação em C#)](https://docs.microsoft.com/pt-br/dotnet/csharp/programming-gue/types/) 

Tipos, variáveis e valores

O C# é uma linguagem fortemente tipada. Todas as variáveis e constantes têm um tipo, assim como cada expressão que é avaliada como um valor. Cada declaração de método especifica um nome, número de parâmetros e tipo e espécie (valor, referência ou saída) para cada parâmetro de entrada e para o valor de retorno. A biblioteca de classes .NET define um conjunto de tipos numéricos internos e tipos mais complexos que representam uma ampla variedade de constructos lógicos, como o sistema de arquivos, conexões de rede, coleções e matrizes de objetos e datas. Um programa C# típico usa tipos da biblioteca de classes e dos tipos definidos pelo usuário que modelam os conceitos específicos para o domínio do problema do programa.
As informações armazenadas em um tipo podem incluir os seguintes itens:

O espaço de armazenamento que uma variável do tipo requer.

Os valores mínimo e máximo que ele pode representar.

Os membros (métodos, campos, eventos e etc.) que ele contém.

O tipo base do qual ele herda.

As interfaces que ela implementa.

O local no qual a memória para as variáveis será alocada em tempo de execução.

Os tipos de operações que são permitidos.

O compilador usa informações de tipo para garantir que todas as operações executadas em seu código sejam de tipo seguro. Por exemplo, se você declarar uma variável do tipo int, o compilador permitirá que você use a variável nas operações de adição e subtração. Se você tentar executar as mesmas operações em uma variável do tipo bool, o compilador gerará um erro, como mostrado no exemplo a seguir:

**C#**

```int a = 5; int b = a + 2; //OK bool test = true; // Error. Operator '+' cannot be applied to operands of type 'int' and 'bool'. int c = a + test;```

 Observação
Desenvolvedores de C e C++, observem que, em C#, bool não é conversível em int.

O compilador insere as informações de tipo no arquivo executável como metadados. O CLR (Common Language Runtime) usa esses metadados em tempo de execução para assegurar mais segurança de tipos ao alocar e recuperar a memória.

Especificando tipos em declarações de variável

Quando declara uma variável ou constante em um programa, você deve especificar o tipo da variável ou usar a palavra-chave var para permitir que o compilador infira o tipo. O exemplo a seguir mostra algumas declarações de variáveis que usam tipos numéricos internos e tipos complexos definidos pelo usuário:

```// Declaration only:
float temperature;
string name;
MyClass myClass;

// Declaration with initializers (four examples):
char firstLetter = 'C';
var limit = 3;
int[] source = { 0, 1, 2, 3, 4, 5 };
var query = from item in source
            where item <= limit
            select item;```

(...)
