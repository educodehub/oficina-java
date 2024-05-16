# Avançando em Java

Neste material, vamos revisar os conteúdos vistos na aula passada e introduzir conceitos mais  avançados na linguagem de programação Java. 

## Arrays em Java

Em Java, arrays são estruturas de dados homogêneas que armazenam um único tipo de dado. Eles são úteis quando precisamos armazenar uma coleção de valores em uma única variável, em vez de declarar várias variáveis separadas para cada valor. Além disso, em Java, os arrays são considerados objetos de tamanho fixo, o que significa que o tamanho do array deve ser declarado no momento da sua criação e não pode ser alterado posteriormente.

### Arrays Unidimensionais

Os arrays unidimensionais, também conhecidos como vetores, armazenam elementos em uma única dimensão. Cada elemento é acessado por um índice numérico que começa do zero. Aqui está como você declara, inicializa e acessa um array unidimensional em Java:

#### Declaração e Inicialização:

```java
int[] vetor = {4, 5, 1, 7}; // Inicialização com valores pré-definidos

int[] vetor = new int[4]; // Definindo o comprimento do array
```

#### Acesso aos Elementos:

```java
int primeiroElemento = vetor[0]; // Acessando o primeiro elemento
int segundoElemento = vetor[1]; // Acessando o segundo elemento
```

#### Como Percorrer um Array:

Você pode percorrer um array usando um loop `for`:

```java
for (int i = 0; i < vetor.length; i++) {
    System.out.println("Elemento " + i + ": " + vetor[i]);
}
```

#### Métodos Úteis:

Alguns métodos úteis para trabalhar com arrays unidimensionais incluem:

- `Arrays.sort()`: Classifica os elementos do array em ordem crescente.
- `Arrays.toString()`: Converte o array em uma string, útil para impressão.
- `Arrays.copyOf()`: Cria uma cópia do array original com um tamanho especificado.

Aqui estão exemplos de como usar esses métodos:

```java
int[] numeros = {4, 2, 7, 1, 5};

// Classificando os elementos do array em ordem crescente
Arrays.sort(numeros);
System.out.println("Array ordenado: " + Arrays.toString(numeros));

// Convertendo o array em uma string para impressão
System.out.println("Array como string: " + Arrays.toString(numeros));

// Criando uma cópia do array original com um tamanho específico
int[] copiaNumeros = Arrays.copyOf(numeros, 3);
System.out.println("Cópia do array: " + Arrays.toString(copiaNumeros));
```

### Arrays Multidimensionais

Os arrays multidimensionais permitem armazenar elementos em múltiplas dimensões, como matrizes. Eles são declarados, inicializados e acessados de forma um pouco diferente dos arrays unidimensionais:

#### Declaração e Inicialização:

```java
int[][] matriz = {{1, 2, 3}, {4, 5, 6}, {7, 8, 9}}; // Inicialização com valores pré-definidos

int[][] matriz = new int[3][3]; // Definindo o tamanho da matriz
```

#### Acesso aos Elementos:

```java
int elemento = matriz[1][2]; // Acessando o elemento na segunda linha e terceira coluna
```

#### Como Percorrer uma Matriz:

Você pode percorrer uma matriz usando loops `for` aninhados:

```java
for (int i = 0; i < matriz.length; i++) {
    for (int j = 0; j < matriz[i].length; j++) {
        System.out.println("Elemento [" + i + "][" + j + "]: " + matriz[i][j]);
    }
}
```

#### Métodos Úteis:

Alguns métodos úteis para trabalhar com arrays multidimensionais incluem os mesmos métodos úteis para arrays unidimensionais, bem como:

- `Arrays.deepToString()`: Converte um array multidimensional em uma string, incluindo arrays internos.
- `Arrays.equals()`: Verifica se dois arrays multidimensionais são iguais.

Exemplo de uso:

```java
int[][] matriz = {{1, 2, 3}, {4, 5, 6}, {7, 8, 9}};

// Convertendo o array multidimensional em uma string para impressão
System.out.println("Matriz como string: " + Arrays.deepToString(matriz));

// Verificando se dois arrays multidimensionais são iguais
int[][] outraMatriz = {{1, 2, 3}, {4, 5, 6}, {7, 8, 9}};
boolean saoIguais = Arrays.deepEquals(matriz, outraMatriz);
System.out.println("As matrizes são iguais? " + saoIguais);
```

Arrays são uma parte fundamental da programação em Java e são amplamente utilizados em muitos tipos de aplicações.

## Manipulação de Strings em Java

Em Java, a manipulação de strings desempenha um papel crucial em muitos aspectos da programação, desde a interação com o usuário até a formatação de saída e o processamento de dados. Vamos explorar alguns dos métodos mais comuns para manipulação de strings, detalhando suas funcionalidades e parâmetros quando necessário.

### Método `toLowerCase()`

O método `toLowerCase()` é usado para converter todos os caracteres de uma string para minúsculas. Isso é útil quando você deseja normalizar o texto e garantir que todas as comparações sejam feitas sem diferenciação entre maiúsculas e minúsculas.

**Exemplo:**

```java
String textoOriginal = "Olá, Mundo!";
String textoEmLowerCase = textoOriginal.toLowerCase();
System.out.println("Texto em LowerCase: " + textoEmLowerCase);
```

**Saída:**

```
Texto em LowerCase: olá, mundo!
```

### Método `toUpperCase()`

O método `toUpperCase()` faz o oposto do `toLowerCase()`, convertendo todos os caracteres de uma string para maiúsculas. Isso pode ser útil ao exibir texto em formato de título ou em situações onde maiúsculas são necessárias.

**Exemplo:**

```java
String textoOriginal = "Olá, Mundo!";
String textoEmUpperCase = textoOriginal.toUpperCase();
System.out.println("Texto em UpperCase: " + textoEmUpperCase);
```

**Saída:**

```
Texto em UpperCase: OLÁ, MUNDO!
```

### Método `trim()`

O método `trim()` remove os espaços em branco no início e no final de uma string. Isso é particularmente útil ao lidar com entradas de usuário, onde espaços extras podem ser acidentalmente incluídos.

**Exemplo:**

```java
String texto = "   Olá, Mundo!   ";
String textoFormatado = texto.trim();
System.out.println("Texto formatado: '" + textoFormatado + "'");
```

**Saída:**

```
Texto formatado: 'Olá, Mundo!'
```

### Método `substring()`

O método `substring()` permite extrair uma parte específica de uma string com base nos índices especificados. Ele aceita um índice inicial e um índice final, onde o caractere após o índice final não é incluído na substring resultante.

**Exemplo:**

```java
String texto = "Java é incrível!";
String textoExtraido = texto.substring(7, 15);
System.out.println("Texto extraído: " + textoExtraido);
```

**Saída:**

```
Texto extraído: incrível
```

### Método `replace()`

O método `replace()` substitui todas as ocorrências de uma substring por outra substring. Isso é útil para fazer substituições simples em uma string.

**Exemplo:**

```java
String texto = "abc ABC def DEF abcd ABCD";
String novoTexto = texto.replace("abc", "xyz");
System.out.println("Texto modificado: " + novoTexto);
```

**Saída:**

```
Texto modificado: xyz ABC def DEF xyzd ABCD
```

### Método `indexOf()`

O método `indexOf()` retorna o índice da primeira ocorrência de uma substring dentro de uma string. Se a substring não for encontrada, ele retorna -1.

**Exemplo:**

```java
String texto = "A terra é azul, como uma laranja.";
int indice = texto.indexOf("azul");
System.out.println("Índice da palavra 'azul': " + indice);
```

**Saída:**

```
Índice da palavra 'azul': 10
```

### Método `split()`

O método `split()` divide uma string em substrings com base em um delimitador especificado e retorna um array contendo as partes resultantes.

**Exemplo:**

```java
String texto = "Esta é uma frase de exemplo.";
String[] palavras = texto.split(" ");
for (String palavra : palavras) {
    System.out.println("Palavra: " + palavra);
}
```

**Saída:**

```
Palavra: Esta
Palavra: é
Palavra: uma
Palavra: frase
Palavra: de
Palavra: exemplo.
```

Esses métodos são fundamentais para manipulação eficiente de Strings em Java, oferecendo flexibilidade e controle sobre o texto em suas aplicações. Entender como e quando usar esses métodos pode melhorar significativamente a manipulação de Strings em seus programas.

## Métodos II

Na aula anterior, discutimos os conceitos básicos de métodos em Java, incluindo sua declaração,  modificadores de acesso, parâmetros e retorno. Agora, vamos aprofundar esses conceitos e explorar exemplos práticos de criação e chamada de métodos, bem como métodos com e sem retorno e a importância da modularização do código.

### Revisão de Conceitos Básicos de Métodos

#### Declaração de Método

Um método em Java é declarado com a seguinte estrutura:

```java
<modificador> <tipo de retorno> <nome do método>(<parâmetros>) {
    // Corpo do método
}
```

- `<modificador>`: indica as propriedades do método, como `public`, `private`, `protected` ou `static`.
- `<tipo de retorno>`: especifica o tipo de dado que o método retorna, ou `void` se o método não retornar nenhum valor.
- `<nome do método>`: identificador do método.
- `<parâmetros>`: variáveis que o método recebe como entrada.

### Exemplos Práticos de Criação e Chamada de Métodos

Aqui estão exemplos práticos de como criar e chamar métodos em Java:

```java
public class ExemploMetodos {
    
    public static void main(String[] args) {
        saudacao(); // Chamando o método saudacao
        int resultado = soma(5, 3); // Chamando o método soma
        System.out.println("O resultado da soma é: " + resultado);
    }
    
    // Método sem retorno e sem parâmetros
    public static void saudacao() {
        System.out.println("Olá, mundo!");
    }
    
    // Método com retorno e parâmetros
    public static int soma(int a, int b) {
        return a + b;
    }
}
```

### Demonstração de Métodos com e sem Retorno

Os métodos podem ter ou não ter retorno. Lembrando que métodos sem retorno são inscritos com a keyword `void`. Aqui está um exemplo de cada:

```java
// Método sem retorno
public static void imprimirMensagem(String mensagem) {
    System.out.println(mensagem);
}

// Método com retorno
public static int calcularSoma(int a, int b) {
    return a + b;
}
```

### A Importância de Utilizar o Modificador `static`

Quando um método é declarado com o modificador `static`, isso significa que ele pertence à classe em si, e não a uma instância específica dessa classe. Isso significa que você pode chamar o método diretamente através do nome da classe, sem precisar criar uma instância da classe antes.

Por exemplo, se temos um método `static` em uma classe chamada `MinhaClasse`, podemos chamá-lo diretamente assim: `MinhaClasse.meuMetodo()`, sem precisar instanciar sua classe desse modo `MinhaClasse objeto = new MinhaClasse()` .

### O Que Acontece Se Não Usarmos o Modificador `static`

Se um método não é declarado como `static`, isso significa que ele é um método de instância, ou seja, você só pode chamar o método em uma instância específica da classe.

Por exemplo, se temos um método `non static` em uma classe chamada `MinhaClasse`, precisamos criar uma instância da classe antes de chamar o método:

```java
MinhaClasse objeto = new MinhaClasse();
objeto.meuMetodo();
```

Sem o modificador `static`, o método só pode ser acessado através de uma instância da classe, não diretamente através do nome da classe. Isso significa que o método depende do estado de uma instância específica da classe.

### Importância da Modularização do Código

A modularização do código, por meio de métodos, é fundamental para desenvolver programas Java eficientes, legíveis e fáceis de manter. Aqui estão algumas razões pelas quais a modularização do código é importante:

1. **Organização e Estruturação**: Dividir o código em métodos permite organizar e estruturar o programa de forma lógica e clara. Cada método pode ser responsável por uma tarefa específica, o que torna o código mais fácil de entender e de dar manutenção.
2. **Reutilização de Código**: A modularização do código facilita a reutilização de funcionalidades em diferentes partes do programa. Uma vez que um método é criado e testado, ele pode ser chamado sempre que necessário em diferentes partes do código, sem a necessidade de reescrever o mesmo código várias vezes.
3. **Facilidade de Manutenção**: Ao dividir o código em métodos pequenos e focados em uma única tarefa, torna-se mais fácil identificar e corrigir problemas quando surgem. Cada método é uma unidade isolada de funcionalidade, o que facilita a identificação e a correção de bugs.
4. **Escalabilidade e Flexibilidade**: A modularização do código permite que o programa seja facilmente escalável e adaptável a mudanças futuras. Novos métodos podem ser adicionados ou modificados sem afetar o restante do código, desde que os métodos existentes sejam bem encapsulados e tenham interfaces claras.
5. **Colaboração**: Em projetos de desenvolvimento de software em equipe, a modularização do código permite que os membros da equipe trabalhem de forma independente em diferentes partes do programa, sem interferir no trabalho dos outros. Cada membro da equipe pode se concentrar em desenvolver e testar seus próprios métodos, facilitando a colaboração e o trabalho em equipe.

Em resumo, a modularização do código por meio de métodos é uma prática fundamental na programação Java, pois torna o código mais organizado, reutilizável, fácil de manter e escalável, nos permitindo desenvolver programas mais robustos e eficientes.

### Utilizando o Debugger em Java

O Debugger é uma ferramenta crucial para os desenvolvedores Java, permitindo inspecionar o comportamento do código durante a execução do programa. Aqui estão os conceitos mais importantes sobre como usar o Debugger em Java:

#### 1. **Pontos de Interrupção (Breakpoints)**

Os pontos de interrupção são fundamentais para controlar onde a execução do programa será pausada. Ao definir um ponto de interrupção em uma linha de código, você pode examinar o estado das variáveis e a execução do programa nesse ponto específico.

#### 2. **Execução Passo a Passo (Step Over, Step Into)**

A capacidade de executar o código passo a passo é essencial para entender o fluxo de execução do programa. Com comandos como "Step Over", você pode avançar para a próxima linha de código sem entrar em métodos, enquanto o "Step Into" permite entrar nos métodos chamados na linha atual para inspecionar seu comportamento.

#### 3. **Inspeção de Variáveis**

Durante a execução do Debugger, você pode monitorar o valor das variáveis em tempo real. Isso é crucial para identificar erros e entender como os valores das variáveis evoluem ao longo do tempo.

#### 4. **Console de Depuração (Debug Console)**

O Console de Depuração fornece uma interface interativa para interagir com o Debugger durante a execução do programa. Aqui você pode avaliar expressões, inspecionar o estado do programa e interagir com o ambiente de depuração.

Dominar esses conceitos básicos do Debugger em Java permitirá que você depure eficientemente seus programas, identificando e corrigindo problemas de forma rápida e eficaz. E se você ficou curioso para usar esta ferramenta poderosa, aqui está um link de como podemos usar o [Debbuger](https://youtu.be/Oq_T4MdyVWs?si=mu5kOnEkArHv6IDl) na IDE Eclipse.

**Até Logo!**

Espero que este material pré-aula sobre Java tenha sido útil e tenha despertado sua curiosidade para aprender mais. Nos vemos na aula! Se você tiver alguma dúvida, não hesite em perguntar durante a aula. Até lá! 🚀👋
