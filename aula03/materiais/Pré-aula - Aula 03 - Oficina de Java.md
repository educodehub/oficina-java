# Programação Orientada a Objetos com Java

Neste material, vamos avançar um pouco mais na linguagem Java e aprender sobre o paradigma da Programação Orientada a Objetos (POO), explorando como utilizar esse paradigma nessa linguagem de programação.

## Introdução

Programação Orientada a Objetos (POO) é um padrão de desenvolvimento de software que estabelece um conjunto de características e princípios que definem como uma linguagem de programação opera e resolve problemas. **Java** e **C#** são exemplos de linguagens que aderem fortemente a esse paradigma.

### Vantagens da Programação Orientada a Objetos

A POO nos proporciona várias vantagens, incluindo:

1. **Reutilização de Código:** A capacidade de criar componentes reutilizáveis, diminuindo a necessidade de escrever o mesmo código várias vezes.
2. **Modularidade:** Facilita a divisão de um programa complexo em partes menores e mais gerenciáveis.
3. **Facilidade de Manutenção:** A modularidade do código permite identificar e corrigir bugs mais rapidamente.
4. **Representação do Mundo Real:** Permite a modelagem de sistemas de forma mais próxima ao mundo real, utilizando objetos que representam entidades do mundo real.

## Elementos Fundamentais da POO

Dentro da Programação Orientada a Objetos (POO), temos elementos fundamentais para a definição e implementação de objetos e suas interações. Vamos explorar cada um deles:

### Classes

Classes são estruturas que definem as características e comportamentos dos objetos. Pense em uma classe como um molde. Cada vez que criamos um novo objeto a partir desse molde, esse objeto possui um conjunto de atributos (propriedades) e métodos (ações) que pode realizar. Imagine, por exemplo, uma cadeira. Identificamos uma cadeira como um objeto, e estamos corretos. Uma cadeira possui atributos, ou seja, propriedades como cor, material de fabricação, número de pernas, etc. Esse objeto também possui ações, como sentar na cadeira, movê-la de lugar, ou consertá-la quando apresenta algum defeito. Na POO, funciona da mesma forma: classes possuem atributos, métodos e estado, e os objetos dessas classes têm acesso a todos esses elementos.

Toda vez que criamos um objeto a partir de uma classe específica, dizemos que estamos instanciando essa classe. Para criar um objeto, precisamos primeiro criar essa estrutura. Além de atributos e métodos, classes também possuem construtores, que veremos mais adiante neste material.

Classes em Java são declaradas com a palavra-chave `class` e devem sempre iniciar sua nomenclatura com letras maiúsculas, por exemplo:

```java
public class MinhaClasse {
    ...
}
```

- `public`: Modificador de acesso da nossa classe, define a visibilidade da nossa estrutura dentro do projeto.
- `class`: Palavra-chave que indica ao Java que estamos criando uma nova classe.
- `MinhaClasse`: Nome da nossa classe, começando com uma letra maiúscula.

Dentro das chaves `{}` é onde definimos nossos atributos e métodos, o escopo total da nossa classe.

### Atributos

Atributos são as propriedades que definimos em nossa classe e pertencem a qualquer objeto que instancia a nossa classe. Os atributos são definidos como variáveis em Java, onde precisamos declarar o tipo do atributo, seu nome, e opcionalmente, os valores iniciais. A única diferença aqui é a adição de modificadores de acesso dentro da declaração dos atributos. A presença desses modificadores está relacionada a um dos pilares da POO, o encapsulamento, que veremos em detalhes mais adiante.

Mas como se declara um atributo? Vamos ver um exemplo:

```java
public class Pessoa {
    private String nome;
    private int idade;
}
```

Explicação:

- `public`: Modificador de acesso da nossa classe, define a visibilidade da nossa estrutura dentro do projeto.
- `class`: Palavra-chave que indica ao Java que estamos criando uma nova classe.
- `Pessoa`: Nome da nossa classe. E dentro dessa classe temos:
  - `private`: Modificador de acesso dos atributos `nome` e `idade`, restringindo o acesso direto de fora da classe.
  - `String` e `int`: Tipos de dados dos nossos atributos `nome` e `idade`, respectivamente.
  - `nome` e `idade`: Nomes dos nossos atributos.

Toda vez que criamos um objeto da classe `Pessoa`, os atributos `nome` e `idade` pertencerão a esse objeto, podendo ele modificar esses atributos ou recuperar seus valores através de métodos apropriados (getters e setters).

### Construtores

Construtores são métodos especiais dentro de uma classe, responsáveis por inicializar um novo objeto. Eles possuem o mesmo nome da classe e não têm nenhum tipo de retorno, nem mesmo `void`. Construtores são chamados automaticamente quando criamos um novo objeto (instanciamos nossa classe) e podem ser configurados para assumir valores iniciais ou não.

Construtores se dividem em dois tipos principais:

- **Construtor padrão:** É o construtor sem argumentos, fornecido implicitamente pelo Java se nenhum construtor for definido na classe. Ele não faz nada além de chamar o construtor da superclasse, permitindo a criação de objetos sem a necessidade de inicializar atributos manualmente.
- **Construtor parametrizado:** Permite a adição de parâmetros pelo desenvolvedor, possibilitando a inicialização do objeto com estados específicos, ou seja, com valores iniciais definidos pelos parâmetros.

Quando você não define nenhum construtor, o Java fornece implicitamente um construtor padrão para você. No entanto, se você definir qualquer construtor (seja padrão ou parametrizado), o construtor padrão implícito não será fornecido automaticamente.

#### Exemplos de Construtores

Aqui está um exemplo de como definir um construtor padrão e um construtor parametrizado:

```java
public class Pessoa {
    private String nome;
    private int idade;

    // Construtor padrão
    public Pessoa() {
        // Não faz nada além de permitir a criação de um objeto vazio
    }

    // Construtor parametrizado
    public Pessoa(String nome, int idade) {
        this.nome = nome;
        this.idade = idade;
    }
}
```

Neste exemplo:

- O construtor padrão `Pessoa()` não recebe parâmetros e não faz nada específico além de permitir a criação de um objeto `Pessoa` sem inicializar os atributos.
- O construtor parametrizado `Pessoa(String nome, int idade)` permite criar um objeto `Pessoa` inicializando os atributos `nome` e `idade` com os valores fornecidos.

#### O Papel do `this`

A palavra-chave `this` em Java é uma referência ao próprio objeto atual. Ela é usada para diferenciar entre os atributos da classe e os parâmetros do método ou construtor quando eles têm o mesmo nome. No exemplo acima, `this.nome` e `this.idade` referem-se aos atributos da classe `Pessoa`, enquanto `nome` e `idade` referem-se aos parâmetros do construtor.

Usar `this` é especialmente importante para evitar ambiguidades e garantir que os valores corretos sejam atribuídos aos atributos do objeto. 

```java
public class Pessoa {
    private String nome;
    private int idade;

    // Construtor padrão
    public Pessoa() {
        // Não faz nada além de permitir a criação de um objeto vazio
    }

    // Construtor parametrizado
    public Pessoa(String nome, int idade) {
        this.nome = nome; // Atribui o valor do parâmetro 'nome' ao atributo 'nome' do objeto
        this.idade = idade; // Atribui o valor do parâmetro 'idade' ao atributo 'idade' do objeto
    }
}
```

#### Uso do `super()`

Na nossa IDE Eclipse, há um conjunto de comandos que nos permite implementar um construtor utilizando os campos (atributos) da nossa classe. Toda vez que usamos esse comando, podemos notar algo assim:

```java
public Pessoa(String nome, int idade) {
	super();
	this.nome = nome;
	this.idade = idade;
}
```

Essa estrutura é quase idêntica ao que desenvolvemos anteriormente, exceto pela adição da palavra `super()`. Esse comando é uma chamada ao construtor da superclasse.

Em Java, toda classe herda, direta ou indiretamente, da classe `Object`. Mesmo que uma classe não declare explicitamente a herança de outra classe, ela ainda assim possui uma superclasse, que é a `Object`. O uso do `super()` no construtor da nossa classe `Pessoa` permite chamar o construtor da superclasse, `Object`, inicializando qualquer atributo ou executando qualquer lógica definida no construtor padrão da classe `Object`.

Apesar de, no caso específico da classe `Object`, o uso do `super()` ser opcional (pois o compilador Java insere automaticamente essa chamada se não estiver presente), é uma prática comum e útil em classes que herdam de outras classes, garantindo que a cadeia de herança seja corretamente inicializada.

### Exemplo Prático de Uso de `super()`

Vamos considerar um exemplo mais elaborado para entender melhor o uso de `super()`. Suponha que temos uma classe `Pessoa` e uma subclasse `Estudante`:

```java
public class Pessoa {
    private String nome;
    private int idade;

    public Pessoa(String nome, int idade) {
        this.nome = nome;
        this.idade = idade;
    }
}
```

Agora, definimos a classe `Estudante` que herda de `Pessoa`:

```java
public class Estudante extends Pessoa {
    private String curso;

    public Estudante(String nome, int idade, String curso) {
        super(nome, idade); // chama o construtor da superclasse Pessoa
        this.curso = curso;
    }
}
```

No construtor da classe `Estudante`, usamos `super(nome, idade)` para chamar o construtor da superclasse `Pessoa`. Isso garante que os atributos `nome` e `idade` sejam corretamente inicializados pela superclasse antes de inicializarmos o atributo `curso` específico da classe `Estudante`.

Em resumo, o uso de `super()` é fundamental para assegurar que todas as inicializações de atributos e execuções de lógica necessárias nas superclasses sejam realizadas, promovendo uma construção de objeto consistente e correta na cadeia de herança.

### Métodos

Métodos em Java na Programação Orientada a Objetos (POO) são sub-rotinas ou procedimentos que realizam uma determinada tarefa ou operação. Eles são blocos de código que encapsulam uma funcionalidade específica e são usados principalmente para modularização e reutilização de código. Em Java, todos os métodos devem estar dentro de uma classe, pois não há suporte para métodos globais.

#### Declaração de Métodos e Métodos Get/Set

Para entender como os métodos funcionam e como são declarados, vamos usar como exemplo os métodos acessores que mencionamos no tópico [Atributos](###Atributos), os chamados "getters" e "setters".

Os métodos acessores são usados para acessar os atributos de uma classe. Com os "getters", podemos recuperar o valor de um determinado campo que definimos em nossa classe. Por exemplo, na classe `Pessoa`, podemos criar o método acessor `getNome()`:

```java
public String getNome() {
    return this.nome;
}
```

Nesta estrutura:

- `public`: É o modificador de acesso do nosso método, indicando que ele pode ser acessado por qualquer classe.
- `String`: É o tipo de retorno do nosso método. Observe que o tipo de retorno de um método "getter" deve ser igual ao tipo de dado do atributo correspondente.
- `getNome`: É o nome do nosso método. Por convenção, "getters" são nomeados como `get` + `Nome do Atributo`.
- `return this.nome`: Retorna o valor armazenado no atributo `nome` da classe. O `this` é utilizado para referenciar o próprio objeto no qual o método está sendo chamado.

Além dos "getters", temos os "setters", que são métodos utilizados para modificar o valor de um atributo da classe. Por exemplo, na classe `Pessoa`, podemos criar o método modificador `setNome(String nome)`:

```java
public void setNome(String nome) {
    this.nome = nome;
}
```

Nesta estrutura:

- `public`: É o modificador de acesso do nosso método, indicando que ele pode ser acessado por qualquer classe.
- `void`: Indica que o método não retorna nenhum valor.
- `setNome`: É o nome do nosso método. Por convenção, "setters" são nomeados como `set` + `Nome do Atributo`.
- `String nome`: É o parâmetro do método, que representa o novo valor a ser atribuído ao atributo `nome` da classe.
- `this.nome = nome`: Atribui o valor do parâmetro `nome` ao atributo `nome` da classe. O `this` é utilizado para referenciar o próprio objeto no qual o método está sendo chamado.

Se formos olhar de uma forma geral, visto todos esses conceitos, temos um código parecido com esse:

```java
public class Pessoa {
    private String nome;
    private int idade;

    // Construtor padrão
    public Pessoa() {
        // Não faz nada além de permitir a criação de um objeto vazio
    }

    // Construtor parametrizado
    public Pessoa(String nome, int idade) {
        this.nome = nome; 
        this.idade = idade;
    }
    // Método get do atributo nome
    public String getNome(){
    	return this.nome;
    }
    // Método set do atributo Nome
    public void setNome(String nome){
    	this.nome = nome;
    }
    // Método get do atributo idade
    public int getIdade(){
    	return this.idade;
    }
    // Método set do atributo idade
    public void setIdade(int idade){
    	this.idade = idade;
    }
}
```

### Objetos

Bom, mas e agora, o que são de fato os **objetos** que tanto mencionamos? Objetos são instâncias concretas de classes e representam entidades do mundo real no seu código. Eles possuem atributos, métodos e estado, encapsulando dados e comportamentos que definem essas entidades. Objetos permitem que você estruture seu código de maneira organizada, modularize suas funcionalidades e reutilize componentes de forma eficiente.

#### Criando e Usando Objetos

Para criar um objeto de uma classe, utilizamos a palavra-chave `new` seguida do nome da classe e, se necessário, passamos os parâmetros esperados pelo construtor. Vamos criar alguns objetos da classe `Pessoa` e usar seus métodos:

```java
public class Main {
    public static void main(String[] args) {
        // Criando um objeto usando o construtor padrão
        Pessoa pessoa1 = new Pessoa();
        pessoa1.setNome("João");
        pessoa1.setIdade(30);

        // Criando um objeto usando o construtor parametrizado
        Pessoa pessoa2 = new Pessoa("Maria", 25);

        // Usando os métodos get para acessar os valores dos atributos
        System.out.println("Nome da Pessoa 1: " + pessoa1.getNome()); // Saída: João
        System.out.println("Idade da Pessoa 1: " + pessoa1.getIdade()); // Saída: 30
        System.out.println("Nome da Pessoa 2: " + pessoa2.getNome()); // Saída: Maria
        System.out.println("Idade da Pessoa 2: " + pessoa2.getIdade()); // Saída: 25
    }
}
```

Neste exemplo:

- `pessoa1` é criada usando o construtor padrão e, em seguida, os métodos `setNome()` e `setIdade()` são usados para definir seus atributos.
- `pessoa2` é criada usando o construtor parametrizado, inicializando diretamente os atributos `nome` e `idade` com os valores fornecidos.
- Os métodos `getNome()` e `getIdade()` são usados para acessar e imprimir os valores dos atributos dos objetos.

#### Benefícios dos Objetos

- **Encapsulamento:** Objetos encapsulam dados e métodos, escondendo detalhes internos e expondo apenas o que é necessário através de métodos públicos. Isso promove a segurança e a integridade dos dados.
- **Reutilização:** Uma vez definidas, as classes podem ser reutilizadas para criar múltiplos objetos. Isso economiza tempo e esforço na escrita de código.
- **Modularização:** Objetos ajudam a modularizar seu código, permitindo que diferentes partes de um programa sejam desenvolvidas e testadas independentemente.
- **Abstração:** Objetos permitem representar conceitos complexos do mundo real de forma mais compreensível e manipulável no código.

Em resumo, objetos são fundamentais na POO, pois permitem que você estruture seu código de maneira clara, modular, e reutilizável, refletindo entidades do mundo real com suas características e comportamentos específicos.

### A classe Object

Falamos mais cedo que todas as classes herdavam da classe raiz `Object`, mas o que seria essa classe? A classe `Object` é a raiz da hierarquia de classes em Java. Cada classe definida herda implicitamente de `Object` se não especificar outra superclasse. Isso significa que todos os objetos em Java, independentemente de sua classe, têm `Object` como um ancestral. A classe `Object` fornece métodos fundamentais que podem ser utilizados ou sobrescritos pelas subclasses. Entre esses métodos, destacam-se `toString`, `equals` e `hashCode`.

#### Método `toString`

O método `toString` é utilizado para fornecer uma representação em forma de string do objeto. A implementação padrão deste método na classe `Object` retorna uma string que consiste no nome da classe do objeto, seguido por um sinal de arroba (@) e o valor hexadecimal do código de hash do objeto. Esta implementação geralmente não é muito útil para propósitos práticos, e é comum sobrescrever o método `toString` para fornecer uma representação mais significativa do objeto.

Exemplo de sobrescrita do método `toString`:

```Java
public class Pessoa {
    private String nome;
    private int idade;

    public Pessoa(String nome, int idade) {
        this.nome = nome;
        this.idade = idade;
    }

    @Override
    public String toString() {
        return "Pessoa[nome=" + nome + ", idade=" + idade + "]";
    }
}
```

#### Método `equals`

O método `equals` é utilizado para comparar a igualdade de dois objetos. A implementação padrão deste método na classe `Object` verifica se as referências dos objetos são iguais, ou seja, se os dois objetos comparados são o mesmo objeto na memória. Para comparar o conteúdo dos objetos, é necessário sobrescrever este método.

Exemplo de sobrescrita do método `equals`:

```java
public class Pessoa {
    private String nome;
    private int idade;

    public Pessoa(String nome, int idade) {
        this.nome = nome;
        this.idade = idade;
    }

    @Override
    public boolean equals(Object obj) {
        if (this == obj) return true;
        if (obj == null || getClass() != obj.getClass()) return false;
        Pessoa pessoa = (Pessoa) obj;
        return idade == pessoa.idade && nome.equals(pessoa.nome);
    }
}
```

#### Método `hashCode`

O método `hashCode` retorna um valor inteiro que é utilizado para a dispersão dos objetos em coleções baseadas em hash, como `HashMap` e `HashSet`. A implementação padrão na classe `Object` gera um código baseado no endereço do objeto na memória. Para garantir que objetos iguais (segundo o método `equals`) tenham o mesmo código de hash, é necessário sobrescrever este método sempre que o método `equals` for sobrescrito.

Exemplo de sobrescrita do método `hashCode`:

```java
public class Pessoa {
    private String nome;
    private int idade;

    public Pessoa(String nome, int idade) {
        this.nome = nome;
        this.idade = idade;
    }

    @Override
    public int hashCode() {
        return Objects.hash(nome, idade);
    }
}
```

A classe `Object` é fundamental no Java, fornecendo métodos essenciais como `toString`, `equals` e `hashCode` que são frequentemente sobrescritos para fornecer comportamentos específicos e úteis:

- **`toString`**: Fornece uma representação em string do objeto.
- **`equals`**: Compara a igualdade de dois objetos.
- **`hashCode`**: Retorna um código de hash para o objeto, importante para coleções baseadas em hash.

Sobrescrever esses métodos de forma adequada é crucial para garantir a correta funcionalidade e desempenho dos objetos nas diversas operações e estruturas de dados em Java.

### Os 4 Pilares da Programação Orientada a Objetos (POO)

A Programação Orientada a Objetos (POO) é um paradigma de programação que organiza o software em objetos que encapsulam dados e comportamentos. Existem quatro pilares fundamentais que sustentam a POO, cada um contribuindo para a criação de software modular, reutilizável e fácil de manter. Esses pilares são: Abstração, Encapsulamento, Herança e Polimorfismo. No entanto, para esta aula só veremos os dois primeiros.

#### 1. Abstração

Abstração é o processo de simplificar a complexidade, destacando os aspectos essenciais de uma entidade e ignorando os detalhes irrelevantes. Em termos práticos, abstração nos permite definir classes que representam conceitos gerais, sem se preocupar com a implementação concreta em um primeiro momento. A essência da abstração é a possibilidade dos desenvolvedores de criarem modelos simplificados de entidades complexas do mundo real, focando apenas nos aspectos mais importantes da aplicação desenvolvida.

- **Exemplo:** Considere a classe `Carro`. Um carro tem atributos como `marca`, `modelo`, e `ano`, e métodos como `acelerar()` e `frear()`. A classe `Carro` abstrai a ideia de um carro sem entrar em detalhes específicos de como, por exemplo, o motor é implementado.

```java
public abstract class Carro {
    private String marca;
    private String modelo;
    private int ano;

    public abstract void acelerar();
    public abstract void frear();
}
```

#### 2. Encapsulamento

Encapsulamento é o mecanismo de restringir o acesso direto a alguns dos componentes de um objeto, protegendo os dados e garantindo a integridade dos mesmos. Através do encapsulamento, controlamos como os dados são acessados e modificados, geralmente utilizando métodos `get` e `set`.

- **Exemplo:** Na classe `Pessoa`, os atributos `nome` e `idade` são privados e só podem ser acessados ou modificados através dos métodos públicos `getNome()`, `setNome()`, `getIdade()` e `setIdade()`.

```java
public class Pessoa {
    private String nome;
    private int idade;

    public String getNome() {
        return nome;
    }

    public void setNome(String nome) {
        this.nome = nome;
    }

    public int getIdade() {
        return idade;
    }

    public void setIdade(int idade) {
        this.idade = idade;
    }
}
```

O encapsulamento funciona com o uso de modificadores de acesso, que faz justamente essa restrição aos componentes do código. Esses modificadores é que garantem que somente as classes apropriadas possam acessar as informações. Os modificadores mais comum são:

- **private** — os atributos e os métodos marcados como “private” só podem ser acessados dentro da própria classe em que foram declarados;
- **protected** — os atributos e os métodos marcados como “protected” podem ser acessados dentro da própria classe e das subclasses;
- **public** — os atributos e os métodos marcados como “public” podem ser acessados por qualquer classe.

### Resumo

- **Abstração:** Simplificação da complexidade, focando nos aspectos essenciais.
- **Encapsulamento:** Proteção dos dados, controlando o acesso e modificação através de métodos.

Esses foram os dois primeiros pilares da programação Orientada a Objetos. Na próxima aula veremos os últimos dois, e como os quatro juntos montam e estruturam esse paradigma, permitindo a criação de programas mais complexos.

**Até Logo!**

Espero que este material pré-aula sobre Java tenha sido útil e tenha despertado sua curiosidade para aprender mais. Nos vemos na aula! Se você tiver alguma dúvida, não hesite em perguntar durante a aula. Até lá! 🚀👋	
