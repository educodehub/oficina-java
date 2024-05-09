# Introdução a programação em Java

Neste material, vamos abordar os conceitos fundamentais da linguagem de programação Java e os elementos essenciais do ambiente de desenvolvimento dessa linguagem.

## Plataforma Java

Java é uma linguagem de programação orientada a objeto, multiplataforma, criada por James Gosling e liberada pela primeira vez pela Sun Microsystens. Uma curiosidade: A linguagem inicialmente foi chamada de Oak, no entanto, já existia um domínio com este mesmo nome. Percebendo a adversidade, o time do Green Project, liderado por James Gosling, resolveu nomear a linguagem com o nome de um café adorado por todos, o café Java, cujos grãos proviam da ilha de Java.

Como dito anteriormente, Java é multiplataforma, ou seja, além da linguagem, o programador conta com um conjunto de APIs que facilitam o desenvolvimento de suas aplicações. A **Java SE** é a plataforma que vamos usar durante toda nossa oficina. Ela representa a base do Java, sendo composta pelas APIs e bibliotecas básicas para possibilitar o desenvolvimento de aplicativos de linha de comando e desktop. Além da Java SE, existem algumas outras, como **Java EE** e **Java ME**, embora não tão relevantes para o nosso propósito.

## JRE, JDK e JVM

Outro ponto relevante a se destacar são algumas tecnologias responsáveis pela execução, desenvolvimento e compilação de códigos em Java.

- JRE: Java Runtime Enviroment (Ambiente de Execução Java), é a tecnologia necessária para rodar nossos programas nessa linguagem.
- JDK: Java Development Kit (Kit de Desenvolvimento Java), é o conjunto de ferramentas que nos possibilita desenvolver e executar códigos em Java.
- JVM: Java Virtual Machine (Máquina Virtual Java), a responsável por executar o bytecode Java

## Compilação em Java

Aproveitando que acabamos de ver o conceito da JVM, vamos dar uma olhada rápida no processo de compilação de código Java.

Essa linguagem na verdade é uma mescla de compilação com interpretação. Quando escrevemos código nativo em Java, nosso arquivo possui a extensão **.java**. Entretanto, a nossa JVM não entende esse tipo de linguagem, por isso precisamos fazer uma compilação anterior. Essa compilação é feita pelo compilador Java, o **javac**, incluso dentro do seu JDK. 

Após essa compilação, o que é gerado é um arquivo com o mesmo nome do anterior, mas com a extensão **.class**. Esse arquivo contém bytecodes. São esses bytecodes que a JVM consegue entender, e aí acontece o nosso processo de interpretação. Durante a execução do seu programa, a JVM interpreta o bytecode gerado, executando linha por linha. Uma vantagem do Java é o que chamamos de **"write once, run anywhere"**. Quando um programa Java é compilado e convertido em linguagem de máquina (bytecodes), o arquivo gerado pode ser executado em qualquer máquina e qualquer sistema operacional que possua a JVM, sem a necessidade de um compilador específico para cada máquina.

![compilação_java](https://github.com/cavalcantgus/oficina-de-python/assets/142106838/e4b90a4f-4786-4403-ab8d-4189d79190e6)

## Preparando o ambiente de desenvolvimento Java

Abaixo disponibilizaremos links para tutoriais de instalação do JDK e outros recursos que precisaremos do Java e da IDE Eclipse, que usaremos ao longo de toda nossa oficina.

[Instalação JDK](https://youtu.be/QekeJBShCy4?si=J8546prfwB5UvNU2)

[Instalação Eclipse](https://youtu.be/KWGIaWh71q4?si=WToVzLv3IkvTdTfB)

## Criando seu primeiro programa em Java

Antes de tudo, é importante entender alguns outros conceitos e estruturas de programas em Java.  Então vamos criar um pequeno programa e entender melhor esses conceitos. [Aqui está um tutorial](https://youtu.be/wlt0-1SlBEA?si=3CEbkxPfjhRTU8UF) caso você não se sinta seguro em seguir os passos adiante.

- Abra seu Eclipse e aperte as teclas **CTRL + N**. 
- Na janela que abrir, procure por **Java Project**, clique nessa opção e dê um **Next**. 
- Na próxima janela você deverá nomear o seu projeto. É recomendável a nomeação desse projeto iniciando com letra maiúscula, como **MyProject**. 
- Após isso, clique em **Finish**. 

Você perceberá que apareceu uma pasta na guia lateral esquerda com o nome MyProject. Se você abri-lá, verá uma estrutura mais ou menos assim:

```markdown
- MyProject
	- JRE System Libary [Java-SE XX]
	- src
```

- `MyProject` é o nome do seu projeto Java
- `JRE System Libary [Java-SE XX]` é a biblioteca de recursos que o Java está usando e XX é a versão do seu JSE.
- `src` é a pasta onde ficam todos os pacotes do seu projeto.
- `Pacotes` são um agrupamento de classes. São eles que organizam e modularizam nosso código.

Agora, dentro de `src`, clique com o botão esquerdo do seu mouse e no menu suspenso que abrir, selecione a opção **New -> Package**. Uma janela será aberta. Nomeie seu pacote como **application** e clique em Finish. Pronto, agora temos um pacote e podemos finalmente criar nossa primeira classe. 

- Dentro do seu pacote **application**, clique com o botão esquerdo do mouse, depois em **New -> Class**. 
- Na janela que se abrir, nomeie sua classe como **Hello**.
- Ainda nessa janela, procure a opção **public static void main(String[] args)** e marque-a.
- Clique em Finish.

Você verá algo como:

```java
package application; // Indica o pacote da nossa classe

public class Hello { // Nossa classe Hello

	public static void main(String[] args) {
        /* Nosso método principal
		   O responsável por inicializar qualquer 												   programa Java que temos
		*/
	}
}
```

Essa é a estrutura básica do nosso programa em Java. Agora, dentro do nosso método **main** (Não se preocupe que mais adiante falaremos de métodos), vamos inserir uma linha de código que nos permitirá printar um texto dentro do terminal da nossa IDE. No seu arquivo, digite:

```java
package application; 

public class Hello { 

	public static void main(String[] args) {
       System.out.print("Hello World!");
	}
}
```

Salve o arquivo e em seguida, clique  com o botão esquerdo do mouse no seu arquivo **Hello.java**. No menu suspenso que abrir, vá em **Run as -> Java Application**. Deverá ver a seguinte sáida no seu terminal:

```bash
Hello World!
```

Pronto, você acaba de construir e executar o seu primeiro programa em Java. Meus parabéns!!!

## Saída de dados

No exemplo anterior, criamos um programa básico que exibia a mensagem "Hello World!" na tela. Se você está se perguntando sobre todas aquelas linhas de código e o que significa o comando System.out.print(), é hora de esclarecer algumas coisas.

Em Java, a forma mais comum de apresentar dados na tela é usando o comando:

```java
System.out.print("Hello World!")
```

- `System.out`: refere-se à saída padrão do sistema. Em programas de console, como o nosso exemplo, essa saída padrão geralmente é a tela.
- `print()`: é um método usado para imprimir texto na saída padrão. 

Então, quando executamos `System.out.print("Hello World!);`, a frase "Hello World!" é exibida na tela .

Outra forma de apresentar dados na tela é usando um comando parecido.

```java
System.out.println("Hello World!")
```

O método `println()` funciona de maneira semelhante ao `print()`, mas adiciona automaticamente uma nova linha após imprimir o texto. Então, ao usar `println()`, cada chamada subsequente irá imprimir em uma nova linha.

Por fim, temos um print formatado:

```java
System.out.printf("Exemplo de saída: %s", "valor");
```

O método `printf()` permite a formatação de strings em Java. Você especifica um formato de string, seguido pelos valores que deseja inserir nesse formato. No exemplo acima, `%s` é um marcador de posição que será substituído pelo valor da variável "valor". Essa última forma de saída de dados é muito semelhante à saída de dados na linguagem C.

Uma curiosidade interessante é que Java foi baseado em C, o que explica muitas semelhanças entre as duas linguagens.

## Variáveis

Variáveis são campos que definimos para armazenar dados dentro da memória de forma temporária. Elas só existem durante a execução do programa.

Em Java, variáveis são declaradas da seguinte forma:

```java
<tipo> nome = valor;
```

Onde `<tipo>` é o tipo de dado atribuído à variável, "nome" é o identificador da variável e "valor" é o dado ou informação atribuída a ela. Aqui está um exemplo com os tipos mais comuns em Java:

```java
String nome = "Maria"; // Usado para armazenar dados textuais
int numero = 10; // Usado para armazenar números inteiros
float altura = 1.75f; // Usado para armazenar números decimais de precisão simples
double saldoBancario = 23.85; // Usado para armazenar número decimais de precisão dupla
boolean ligado = true; // Usado para armazenar valores de Verdadeiro ou Falso
```

Uma boa prática na nomeação de variáveis é atribuir nomes significativos a elas, como **idadeDoUsuario**, caso você precise armazenar a idade de alguém. Além disso, em Java, utilizamos o padrão camelCase para nomear variáveis. Isso significa que ao declarar suas variáveis, elas devem começar com letra minúscula e, se forem compostas, a palavra seguinte deve vir junto da palavra anterior, começando com letra maiúscula. Por exemplo:

```java
int idadeDoUsuario;
float alturaEmMetros;
boolean usuarioLogado;
```

## Operações com variáveis

Se quisermos realizar ações com nossas variáveis além de simplesmente declará-las, podemos exibi-las na tela de várias maneiras em Java.

Podemos usar `System.out.println()` para imprimir o valor da variável diretamente:

```java
String nome = "Pedro";
System.out.println(nome); // Saída: Pedro
```

Também podemos usar um print formatado para, por exemplo, cumprimentar um usuário:

```java
String nome = "João";
System.out.printf("Olá %s, prazer em conhecê-lo!", nome);
// Saída: Olá João, prazer em conhecê-lo!
```

Além disso, podemos usar o operador '+' para concatenar nossas variáveis com textos ou realizar operações de soma dentro do nosso método para saída de dados. Por exemplo:

```java
String nome = "Jorge";
int idade = 25;
System.out.println("Este é " + nome + ", e ele tem " + idade + " anos.");
// Saída: Este é Jorge, e ele tem 25 anos.
```

```java
int parcela1 = 10;
int parcela2 = 5;
System.out.println(parcela1 + parcela2);
// Saída: 15
```

Essas são algumas maneiras simples e úteis de interagir com variáveis em Java para exibir informações na tela.

## Operadores aritméticos

Em Java, os operadores aritméticos são utilizados para realizar operações matemáticas em variáveis numéricas. Vamos explorar alguns dos operadores mais comuns:

| Operador | Descrição                 | Exemplo                  |
| -------- | ------------------------- | ------------------------ |
| +        | Adição                    | `int resultado = 5 + 3;` |
| -        | Subtração                 | `int diferenca = 5 - 3;` |
| *        | Multiplicação             | `int produto = 5 * 3;`   |
| /        | Divisão                   | `int quociente = 6 / 2;` |
| %        | Módulo (resto da divisão) | `int resto = 7 % 3;`     |

## Entrada de dados

Até agora, trabalhamos com variáveis em que o valor é definido previamente por nós, programadores. Mas e se quisermos que o usuário digite algum dado e, em seguida, atribuamos esse dado à nossa variável? Isso é muito útil e em Java fazemos isso usando a classe Scanner. Sua sintaxe é a seguinte:

```java
package application; 
import java.util.Scanner;

public class Hello { 
    public static void main(String[] args) {
        System.out.print("Digite seu nome completo: ");
        Scanner entrada = new Scanner(System.in);
        String nomeCompleto = entrada.nextLine();
        
        System.out.println("Seu nome completo é: " + nomeCompleto); 
    }
}

```

Essa estrutura permite que o programa solicite ao usuário uma entrada de dados, armazenada na variável `nomeCompleto` neste caso, usando o método `nextLine()` do objeto Scanner. Em seguida, o programa imprime o nome completo fornecido pelo usuário.

Quanto a estrutura da classe Scanner, temos:

- `import java.util.Scanner;` importa a classe Scanner do pacote `java.util`, permitindo que você use seus métodos para entrada de dados.

- ` Scanner entrada = new Scanner(System.in);` aqui, criamos uma instância (mais adiante na oficina veremos os conceitos de instância, objetos e classes, não se preocupe) da classe Scanner chamada `entrada`. O parâmetro `System.in` indica que queremos ler os dados da entrada padrão do sistema, que geralmente é o teclado. 
- `String nomeCompleto = entrada.nextLine();` aqui, utilizamos o método `nextLine()` do objeto Scanner para ler a próxima linha de entrada do usuário e armazena-lá na variável `nomeCompleto`.

O Scanner é uma ferramenta poderosa em Java para interação com o usuário e entrada de dados em tempo de execução, permitindo que seus programas sejam mais dinâmicos e interativos.

## Conversão de Dados em Java

Em Java, é comum a necessidade de converter tipos de dados de um formato para outro. Isso pode ser útil em várias situações, como entrada de dados do usuário, manipulação de dados em diferentes formatos, entre outros.

### Conversão Explícita e Implícita

Existem dois tipos de conversão de dados em Java: conversão explícita (também conhecida como casting) e conversão implícita.

- **Conversão Explícita (Casting):** É quando você precisa converter um tipo de dado para outro tipo de forma explícita. Isso é feito colocando o tipo desejado entre parênteses antes da expressão que você deseja converter.

  Exemplo:

  ```java
  double d = 10.5;
  int i = (int) d; // Conversão de double para int
  ```

- **Conversão Implícita:** Também conhecida como coerção de tipo, é quando a conversão é feita automaticamente pelo compilador. Isso ocorre quando você atribui um valor de um tipo menor para um tipo maior.

  Exemplo:

  ```java
  int i = 10;
  double d = i; // Conversão implícita de int para double
  ```

### Conversão entre Tipos Primitivos

Em Java, você pode converter entre tipos primitivos usando os métodos de casting ou deixando o próprio Java fazer a conversão.

#### Conversão Numérica

- **int -> double:**

  ```java
  int i = 10;
  double d = (double) i; // Conversão explícita
  ```

- **double -> int:**

  ```java
  double d = 10.5;
  int i = (int) d; // Conversão explícita
  ```

#### Conversão de Caracteres

- **char -> int:**

  ```java
  char c = 'A';
  int ascii = (int) c; // Conversão explícita
  ```

- **int -> char:**

  ```java
  int ascii = 65;
  char c = (char) ascii; // Conversão explícita
  ```

### Conversão entre Tipos de Referência

Além da conversão entre tipos primitivos, em Java também é possível converter entre tipos de referência, como String e outros tipos de objetos.

#### Conversão de String para Números

- **String para int:**

  ```java
  String numeroStr = "10";
  int numero = Integer.parseInt(numeroStr);
  ```

- **String para double:**

  ```Java
  String numeroStr = "10.5";
  double numero = Double.parseDouble(numeroStr);
  ```

#### Conversão de Números para String

- **int para String:**

  ```java
  int numero = 10;
  String numeroStr = Integer.toString(numero);
  ```

- **double para String:**

  ```java
  double numero = 10.5;
  String numeroStr = Double.toString(numero);
  ```

## Operadores de Comparação

| Operador | Descrição                                                    | Exemplo |
| -------- | ------------------------------------------------------------ | ------- |
| >        | Maior que - True se o operando a esquerda for maior que o da direita | x > y   |
| <        | Menor que - True se o operando a esquerda for menor que o da direita | x < y   |
| ==       | Igual - True se ambos os operandos forem iguais              | x == y  |
| !=       | Não Igual - True se os operandos forem diferentes            | x != y  |
| >=       | Maior que ou Igual - True se o operando da esquerda for maior ou igual ao da direita | x >= y  |
| <=       | Menor que ou Igual - True se o operando da esquerda for menor ou igual ao da direita | x <= y  |

## Operadores Lógicos

Operadores Lógicos são usados para combinar comandos condicionais.

| Operador | Descrição                                                    | Exemplo          |
| -------- | ------------------------------------------------------------ | ---------------- |
| `&&`     | Retorna True se ambos os comandos são verdadeiros            | x < y && x < 10  |
| `||`     | Retorna True se um dos comandos é verdadeiro                 | x < y \|\| x > 3 |
| `!`      | Reverte o resultado, retorna false se o resultado for true e vice-versa | !(x > 10)        |

Vamos considerar então alguns exemplos com operadores lógicos:

```java
package application;

public class Hello{
	public static void main(String[] args){
        int n1 = 5;
        int n2 = 10;
        int n3 = 3;
        System.out.println(n1 < n2 && n1 > n3); // true, pois 5 é menor que 10 e maior 													   que 3
        System.out.println(n2 == n3 || n2 < n1); // false, pois 10 não é igual a 3 e nem 												     menor que 5
        System.out.println(!false); // true, pois o que não é falso é verdadeiro
	}
}
```

## Estruturas Condicionais

As estruturas de controle condicionais em Java permitem que você tome decisões com base em condições específicas. As principais construções condicionais são `if`, `else if`, `else`, e `switch case`.

### If

O `if` é usado para executar um bloco de código se uma condição for verdadeira.

**Estrutura:**

```java
if (condição) {
    // Bloco de código a ser executado se a condição for verdadeira
}
```

Exemplo:

```java
String pais = "Brasil";
if (pais == "Brasil") {
    System.out.println("Você é brasileiro");
}
```

### Else if

O `else if` permite verificar várias condições. Se a condição `if` não for verdadeira, ele verifica a próxima condição.

**Estrutura:**

```java
if (condição1) {
    // Bloco de código a ser executado se a condição1 for verdadeira
} else if (condição2) {
    // Bloco de código a ser executado se a condição2 for verdadeira
}
```

Exemplo:

```java
String pais = "Argentina";
if (pais == "Brasil") {
    System.out.println("Você é brasileiro");
} else if (pais == "Argentina") {
    System.out.println("Você é argentino");
}
```

### Else

O `else` é usado quando nenhuma das condições anteriores é verdadeira.

**Estrutura:**

```java
if (condição) {
    // Bloco de código a ser executado se a condição for verdadeira
} else {
    // Bloco de código a ser executado se a condição não for verdadeira
}
```

Exemplo:

```java
String pais = "Argentina";
if (pais == "Brasil") {
    System.out.println("Você é brasileiro");
} else if (pais == "Argentina") {
    System.out.println("Você é argentino");
}
else{
    System.out.println("Você não é nem argentino nem brasileiro");
}
```

### Condicionais Aninhadas

Condicionais aninhadas ocorrem quando uma estrutura condicional está contida dentro de outra. Isso permite uma lógica mais complexa, onde diferentes condições podem ser verificadas em diferentes níveis.

**Estrutura:**

```java
if (condição1) {
    if (condição2) {
        // Bloco de código a ser executado se ambas as condições forem verdadeiras
    } else {
        // Bloco de código a ser executado se a condição1 for verdadeira e a condição2 			   não for
    }
} else {
    // Bloco de código a ser executado se a condição1 não for verdadeira
}
```

**Exemplo:**

```java
int idade = 20;
boolean temCarteira = true;

if (idade >= 18) {
    if (temCarteira) {
        System.out.println("Pode dirigir");
    } else {
        System.out.println("Não pode dirigir, precisa de carteira de motorista");
    }
} else {
    System.out.println("Não pode dirigir, é menor de idade");
}
```

### Switch Case

A estrutura `switch case` é usada quando você tem várias condições diferentes para testar.

**Estrutura:**

```java
switch (expressão) {
    case valor1:
        // Bloco de código a ser executado se expressão for igual a valor1
        break;
    case valor2:
        // Bloco de código a ser executado se expressão for igual a valor2
        break;
    default:
        // Bloco de código a ser executado se expressão não corresponder a nenhum dos 			   valores
}
```

**Exemplo:**

```java
int diaDaSemana = 1;
String nomeDoDia;

switch (diaDaSemana) {
    case 1:
        nomeDoDia = "Domingo";
        break;
    case 2:
        nomeDoDia = "Segunda-feira";
        break;
    case 3:
        nomeDoDia = "Terça-feira";
        break;
    default:
        nomeDoDia = "Dia inválido";
}

System.out.println("O dia da semana é: " + nomeDoDia);
```

### Loops em Java

Os loops são estruturas de controle que permitem executar repetidamente um bloco de código enquanto uma condição específica for verdadeira. Em Java, temos três tipos principais de loops: `for`, `while` e `do-while`.

#### Loop for

O loop `for` é ideal quando você sabe quantas vezes deseja repetir um bloco de código. Ele consiste em três partes: inicialização, condição e atualização. Aqui está a estrutura básica:

```java
for (inicialização; condição; atualização) {
    // bloco de código a ser repetido
}
```

No `for`, a inicialização é onde você define a variável de controle do loop, a condição é a expressão que determina quando o loop deve ser encerrado e a atualização é onde você altera a variável de controle a cada iteração.

Exemplo:

```java
for (int i = 0; i < 5; i++) {
    System.out.println("Número: " + i); // A cada iteração, ele printará o valor da 											   variável i
}
```

#### Loop while

O loop `while` é útil quando você não sabe antecipadamente quantas vezes o loop será executado, mas ele deve continuar enquanto uma condição específica for verdadeira. Aqui está a estrutura básica:

```java
while (condição) {
    // bloco de código a ser repetido
}
```

No `while`, o bloco de código é executado repetidamente enquanto a condição for verdadeira.

Exemplo:

```java
int i = 0;
while (i < 5) {
    System.out.println("Número: " + i); 
    i++; // Incremento manual de i
}
// Enquanto a condição for satisfeita ele 												   printará o valor da variável i
```

#### Loop do-while

O loop `do-while` é semelhante ao `while`, mas garante que o bloco de código seja executado pelo menos uma vez, mesmo que a condição inicial seja falsa. Aqui está a estrutura básica:

```while
do {
    // bloco de código a ser repetido
} while (condição);
```

No `do-while`, o bloco de código é executado pelo menos uma vez e, em seguida, a condição é verificada. Se a condição for verdadeira, o bloco de código continuará a ser executado.

Exemplo:

```java
int i = 0;
do {
    System.out.println("Número: " + i);
    i++;
} while (i < 5);
```

Essas estruturas de loop oferecem flexibilidade para controlar a repetição de um bloco de código em Java, permitindo automatizar tarefas repetitivas de forma eficiente.

### Métodos em Java

Métodos em Java são blocos de código que executam uma determinada tarefa e podem ser chamados para executar essa tarefa sempre que necessário. Eles ajudam a organizar o código em unidades lógicas e a reutilizar funcionalidades em diferentes partes do programa.

#### Declaração de Método

A declaração de um método em Java segue a seguinte estrutura:

```java
<modificador> <tipo de retorno> <nome do método>(<parâmetros>) {
    // Corpo do método
}
```

- `<modificador>`: é opcional e indica as propriedades do método, como `public`, `private`, `protected` ou `static`.
- `<tipo de retorno>`: especifica o tipo de dado que o método retorna, ou `void` se o método não retornar nenhum valor.
- `<nome do método>`: é o identificador do método.
- `<parâmetros>`: são as variáveis que o método recebe como entrada, separadas por vírgula se houver mais de uma.

#### Método Main

O método `main` é o ponto de entrada de um programa Java. Ele é onde a execução do programa começa. Aqui está sua estrutura básica:

```java
public static void main(String[] args) {
    // Corpo do método main
}
```

- `public` é o nosso modificador de acesso.
- `static` é uma palavra-chave que indica que nosso método pode ser acesso sem criar instâncias da nossa classe.
- `void` é o nosso retorno padrão.
- `main` é o nome do nosso método.
- `String[] args` é o nosso parâmetro. Um vetor de Strings que captura argumentos da linha de comando 

#### Outro Exemplo de Método

Aqui está um exemplo simples de um método em Java:

```java
public class MinhaClasse {
    
    public static void main(String[] args) {
        int resultado = soma(5, 3);
        System.out.println("O resultado da soma é: " + resultado);
    }
    
    public static int soma(int a, int b) {
        return a + b;
    }
}
```

Neste exemplo:

- `soma` é o nome do método.
- `public` é o nosso modificador de acesso.
- `int` é o tipo de retorno do método.
- `(int a, int b)` são os parâmetros do método.
- `return a + b;` é a instrução que retorna a soma dos dois parâmetros.

#### Tipos de Retorno e Parâmetros

- Um método pode retornar qualquer tipo de dado, incluindo tipos primitivos, objetos e arrays.
- Um método pode ter zero ou mais parâmetros. Se um método não requer nenhum parâmetro, os parênteses vazios são usados: `public void meuMetodo() {...}`.

#### Modificadores de Acesso

- `public`: O método pode ser acessado de qualquer lugar do seu projeto.
- `private`: O método só pode ser acessado dentro da classe onde foi definido.
- `protected`: O método só pode ser acessado por subclasses e classes do mesmo pacote.
- `default` (sem modificador): O método só pode ser acessado por classes do mesmo pacote.

**Até Logo!**

Espero que este material pré-aula sobre Java tenha sido útil e tenha despertado sua curiosidade para aprender mais. Nos vemos na aula! Se você tiver alguma dúvida, não hesite em perguntar durante a aula. Até lá! 🚀👋
