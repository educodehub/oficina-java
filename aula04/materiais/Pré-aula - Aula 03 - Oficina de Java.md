# Programação Orientada a Objetos com Java

Neste material, vamos avançar um pouco mais na Programação Orientada a Objetos e estudar os últimos dois pilares restantes desse paradigma, bem como alguns outros elementos fundamentais da POO.

## Herança

A herança é o terceiro princípio fundamental da Programação Orientada a Objetos (POO). Em Java, a herança permite criar novas classes a partir de classes já existentes, promovendo a reutilização e a organização do código. As novas classes criadas são conhecidas como subclasses, classes filhas ou classes derivadas, enquanto as classes originais são chamadas de superclasses, classes base ou classes pai. As subclasses herdam propriedades e comportamentos da superclasse, podendo também adicionar ou modificar funcionalidades específicas.

Para entender melhor, vamos considerar um exemplo de uma escola. Imagine que temos três tipos de entidades: alunos, professores e funcionários. Em vez de repetir código para cada tipo de entidade, podemos criar uma classe genérica `Pessoa` que contenha os atributos e métodos comuns a todos. Esse processo de abstrair características comuns para criar uma superclasse é conhecido como **Generalização**.

### Generalização

Generalização é o processo de identificar características comuns a várias classes específicas e consolidá-las em uma única classe base. Essa abordagem ajuda a evitar duplicação de código e promove a reutilização e a organização do código. No nosso exemplo, a classe `Pessoa` representa a generalização das características comuns de alunos, professores e funcionários.

```java
import java.util.Date;

public class Pessoa {
    public String nome;
    public String cpf;
    public Date dataNascimento;

    public Pessoa(String nome, String cpf, Date dataNascimento) {
        this.nome = nome;
        this.cpf = cpf;
        this.dataNascimento = dataNascimento;
    }
}
```

Nesta classe `Pessoa`, temos atributos comuns como `nome`, `cpf` e `dataNascimento`, além de um construtor que inicializa esses atributos. Qualquer pessoa na escola terá esses atributos, portanto faz sentido colocá-los em uma classe base.

### Especialização

Especialização é o processo inverso da generalização. Depois de definir uma classe base, podemos criar subclasses que representam entidades mais específicas, adicionando ou modificando atributos e comportamentos particulares. No nosso exemplo, criamos subclasses `Aluno`, `Professor` e `Funcionario` que herdam da classe `Pessoa`.

```java
import java.util.Date;

public class Aluno extends Pessoa {
    public Aluno(String nome, String cpf, Date dataNascimento) {
        super(nome, cpf, dataNascimento);
    }
}

public class Professor extends Pessoa {
    public Professor(String nome, String cpf, Date dataNascimento) {
        super(nome, cpf, dataNascimento);
    }
}

public class Funcionario extends Pessoa {
    public Funcionario(String nome, String cpf, Date dataNascimento) {
        super(nome, cpf, dataNascimento);
    }
}
```

Aqui, cada uma das subclasses (`Aluno`, `Professor` e `Funcionario`) utiliza a palavra-chave `extends` para indicar que estão herdando da classe `Pessoa`. O construtor de cada subclasse chama o construtor da superclasse usando a palavra-chave `super()`, passando os parâmetros necessários para inicializar os atributos herdados.

### Vantagens da Herança

1. **Reutilização de Código:** A herança permite que subclasses reutilizem o código da superclasse, evitando a duplicação de código.
2. **Hierarquia Clara:** Cria uma hierarquia clara e lógica de classes, facilitando a compreensão e manutenção do código.
3. **Flexibilidade:** Subclasses podem adicionar ou modificar comportamentos específicos, proporcionando flexibilidade no design do sistema.
4. **Facilidade de Manutenção:** Alterações na superclasse são propagadas automaticamente para todas as subclasses, facilitando a manutenção.

### Upcasting e Downcasting

Já vimos que em Java é possível converter de um tipo de dados para outro, seja entre tipos primitivos ou tipos objeto, e isso nós chamamos de **Typecasting**. Em Java, podemos ainda converter um objeto **Pai** em um objeto **Filho** e vice-versa, usando os conceitos de **Upcasting** e **Downcasting**.

#### Upcasting

É o processo de converter uma subclasse para uma superclasse. Este processo é feito automaticamente pelo compilador, uma vez que a subclasse é uma forma especializada da superclasse e, portanto, pode ser tratada como uma instância da superclasse. Upcasting é útil quando queremos tratar um objeto de uma subclasse como um objeto de sua superclasse, geralmente para garantir que um método aceite qualquer objeto que pertença a uma hierarquia de classes.

##### Exemplo de Upcasting

Vamos usar os exemplos anteriores das classes `Pessoa`, `Aluno`, `Professor` e `Funcionario`.

```Java
public class Main {
    public static void main(String[] args) {
        Aluno aluno = new Aluno("João", "123.456.789-00", new Date());
        Professor professor = new Professor("Maria", "987.654.321-00", new Date());
        Funcionario funcionario = new Funcionario("Carlos", "111.222.333-44", new Date());

        // Upcasting - convertendo subclasses para superclasse
        Pessoa pessoa1 = aluno;
        Pessoa pessoa2 = professor;
        Pessoa pessoa3 = funcionario;

        // Agora podemos tratar todos os objetos como instâncias da superclasse Pessoa
        System.out.println("Nome: " + pessoa1.nome);
        System.out.println("Nome: " + pessoa2.nome);
        System.out.println("Nome: " + pessoa3.nome);
    }
}
```

### Downcasting

É o processo inverso de upcasting, onde uma instância de uma superclasse é convertida para uma subclasse específica. Diferente do upcasting, o downcasting precisa ser feito explicitamente e pode causar problemas se não for feito corretamente, pois nem toda instância de uma superclasse é necessariamente uma instância de uma subclasse específica. Para evitar erros, é comum verificar o tipo do objeto usando a palavra-chave `instanceof` antes de realizar o downcasting..

##### Exemplo de Downcasting

Continuando com o exemplo anterior, vamos fazer o downcasting.

```java
public class Main {
    public static void main(String[] args) {
        Aluno aluno = new Aluno("João", "123.456.789-00", new Date());

        // Upcasting
        Pessoa pessoa = aluno;

        // Downcasting - convertendo superclasse para subclasse
        if (pessoa instanceof Aluno) {
            Aluno aluno2 = (Aluno) pessoa;
            System.out.println("Aluno: " + aluno2.nome);
        } else {
            System.out.println("A conversão não é válida.");
        }
    }
}
```

#### Onde são úteis

#### Upcasting

1. **Polimorfismo:** Upcasting é amplamente utilizado em polimorfismo, onde métodos que aceitam objetos da superclasse podem trabalhar com qualquer subclasse, permitindo flexibilidade e reutilização de código.
2. **Coleções:** Ao trabalhar com coleções de objetos que compartilham uma superclasse comum, upcasting permite que todos os objetos sejam armazenados e manipulados de maneira uniforme.
3. **Interface Abstrata:** Facilita o uso de interfaces e classes abstratas, permitindo tratar todas as implementações de maneira uniforme.

#### Downcasting

1. **Acesso a Funcionalidades Específicas:** Downcasting é necessário quando precisamos acessar métodos ou atributos específicos de uma subclasse que não estão disponíveis na superclasse.
2. **Manipulação de Eventos:** Em sistemas baseados em eventos, é comum que eventos sejam tratados de forma genérica e depois convertidos para tipos específicos conforme necessário.
3. **Frameworks e APIs:** Muitas vezes, frameworks e APIs retornam objetos da superclasse e é necessário downcasting para acessar funcionalidades específicas da subclasse.

#### Uso do `instanceof`

A palavra-chave `instanceof` é usada para verificar se um objeto é uma instância de uma classe específica ou de uma subclasse dessa classe. Isso é especialmente útil antes de realizar um downcasting para garantir que a conversão é segura e não causará erros em tempo de execução.

##### Exemplo de `instanceof`

No exemplo de downcasting acima, usamos `instanceof` para verificar se `pessoa` é uma instância de `Aluno` antes de realizar o downcasting.

```java
if (pessoa instanceof Aluno) {
    Aluno aluno2 = (Aluno) pessoa;
    System.out.println("Aluno: " + aluno2.nome);
} else {
    System.out.println("A conversão não é válida.");
}
```

Nesse código, `pessoa instanceof Aluno` retorna `true` se `pessoa` for uma instância de `Aluno` ou de uma subclasse de `Aluno`. Se a verificação passar, o downcasting é realizado de forma segura.

## Polimorfismo

Polimorfismo vem do grego e quer dizer **muitas formas**. Em Java, polimorfismo é o último dos pilares da POO e trata da capacidade de algo assumir diferentes formas. No contexto da Orientação a Objetos, polimorfismo nos mostra como um método pode assumir uma implementação diferente da qual possuía inicialmente. Existem dois principais tipos de polimorfismo:

1. **Polimorfismo de Sobrecarga (Overloading)**: Permite criar múltiplos métodos com o mesmo nome, no entanto, com assinaturas (tipo de retorno e número de parâmetros) diferentes dentro da mesma classe.
2. **Polimorfismo de Sobrescrita (Overriding)**: Permite que uma subclasse forneça uma implementação específica de um método que já está definido na sua superclasse.

### Sobrecarga

A sobrecarga ou **overload** de um método é a capacidade de se implementar vários métodos com o mesmo nome, contanto que a sua lista de parâmetros não seja a mesma para que possa se fazer a separação dos mesmos.

Para entender melhor a sobrecarga, vamos usar o exemplo de uma calculadora. Na nossa classe `Calculadora` teremos o método `soma()` que será sobrecarregado.

```Java
public class Calculadora {
    public int soma(int a, int b) {
        return a + b;
    }

    public double soma(double a, double b) {
        return a + b;
    }

    public int soma(int a, int b, int c) {
        return a + b + c;
    }
}
```

Na classe `Calculadora` possuímos três implementações do método `soma()`, todos com o mesmo nome, no entanto, assinaturas diferentes. Mas como o programa vai saber qual método executar quando `soma()` for chamado? A chamada desse método irá depender do tipo de retorno e quantidade de parâmetros que o método chamado possuir. O programa ao receber a chamada de `soma()` com os parâmetros passados, verificará na classe `Calculadora` em tempo de execução, qual dos seguintes métodos está implementado para receber os parâmetros passados e o convocará.

### Sobreposição

A sobreposição ou **override** de métodos é a capacidade que uma classe Filha tem de sobrescrever a implementação de um método já existente na classe Pai. Diferente da sobrecarga, a sobreposição só funciona se o tipo de retorno, nome e quantidade de parâmetros forem iguais, porém, o método sobreposto pode ser implementado com especificações adicionais da classe Filha, ou não. Para demonstrar, vamos criar uma classe `Animal` e usá-la de exemplo.

```Java
public class Animal {
    public void som() {
        System.out.println("O animal faz um som");
    }
}

public class Cachorro extends Animal {
    @Override
    public void som() {
        System.out.println("O cachorro late");
    }
}

public class Main {
    public static void main(String[] args) {
        Animal meuCachorro = new Cachorro();
        meuCachorro.som();
    }
}
```

Na classe `Animal` definimos um método sem retorno `som()`. Em seguida, criamos a classe `Cachorro`. Note que usamos a palavra-chave `extends` para indicar que essa classe herda de `Animal`. Em consequência dessa herança, nossa classe `Cachorro` agora pode herdar o método `som()` da sua superclasse e sobrescrever esse método, adicionando uma implementação específica. 

A anotação `@Override` é uma anotação de marcador, ela fornece mais informações para o nosso compilador e indica que aquele método em específico está sendo sobrescrito.

### Métodos e Classes `final`

#### Métodos `final`

Um método `final` em Java é um método que não pode ser sobrescrito por subclasses. Isso é útil quando você deseja garantir que a implementação de um método específico não seja alterada, preservando a integridade do comportamento da classe base.

##### Exemplo de Método `final`

```java
public class Animal {
    public final void dormir() {
        System.out.println("O animal está dormindo");
    }
}

public class Cachorro extends Animal {
    // Este código gerará um erro de compilação
    // porque estamos tentando sobrescrever um método final
    @Override
    public void dormir() {
    	System.out.println("O cachorro está dormindo");
    }
}
```

Neste exemplo, a tentativa de sobrescrever o método `dormir` na classe `Cachorro` resultará em um erro de compilação, pois o método `dormir` na classe `Animal` é `final`.

#### Classes `final`

Uma classe `final` é uma classe que não pode ser estendida. Isso é útil quando você deseja garantir que a implementação da classe não possa ser alterada por meio de herança. Toda classe declarada como `final` é sempre uma classe filha, mas jamais pode ser uma classe pai. Pensando numa árvore de classes, a classe `final` seria a última folha dessa nossa árvore, e não sendo permitida a criação de subclasses a partir dela.

##### Exemplo de Classe `final`

```java
public final class Animal {
    public void dormir() {
        System.out.println("O animal está dormindo");
    }
}

// Este código gerará um erro de compilação
// porque estamos tentando estender uma classe final
public class Cachorro extends Animal {
    @Override
	public void dormir() {
    	System.out.println("O cachorro está dormindo");
   }
}
```

Aqui, a tentativa de criar a classe `Cachorro` que estende `Animal` resultará em um erro de compilação, porque a classe `Animal` é `final`.

### Métodos e Classes Abstratas

#### Métodos Abstratos

Um método abstrato é um método declarado, mas não implementado na superclasse abstrata. Qualquer classe que estenda a classe abstrata deve fornecer uma implementação para os métodos abstratos, a menos que a classe filha também seja abstrata. 

```java
public abstract class Animal {
    public abstract void fazerSom(); // Método abstrato

    public void dormir() {
        System.out.println("O animal está dormindo");
    }
}

public class Cachorro extends Animal {
    
    @Override
    public void fazerSom() {
        System.out.println("O cachorro late");
    }
}
```

Neste exemplo, a classe `Animal` tem um método abstrato `fazerSom`. A classe `Cachorro` fornece a implementação concreta para o método `fazerSom`.

**Nota**: Métodos abstratos só podem existir dentro de classe abstratas. No entanto, o contrário não é totalmente verdade, pois classes abstratas podem conter tanto métodos abstratos quanto concretos.

##### Exemplo de Método Abstrato

#### Classes Abstratas

Uma classe abstrata é uma classe que não pode ser instanciada diretamente. Ela é usada como uma base para outras classes. Classes abstratas podem conter métodos abstratos (sem corpo) e métodos concretos (com corpo).

##### Exemplo de Classe Abstrata

```java
public abstract class Animal {
    public abstract void fazerSom(); // Método abstrato

    public void dormir() {
        System.out.println("O animal está dormindo");
    }
}

public class Cachorro extends Animal {
    @Override
    public void fazerSom() {
        System.out.println("O cachorro late");
    }
}

public class Main {
    public static void main(String[] args) {
        // Animal animal = new Animal(); // Erro de compilação: Animal é abstrata e não pode ser instanciada

        Animal meuCachorro = new Cachorro();
        meuCachorro.fazerSom(); // Saída: O cachorro late
        meuCachorro.dormir();   // Saída: O animal está dormindo
    }
}
```

Neste exemplo, você não pode instanciar a classe `Animal` diretamente porque ela é abstrata. No entanto, você pode instanciar a classe `Cachorro` e usar métodos concretos e sobrescritos.

## Interfaces

Uma interface é uma "classe abstrata", comumente utilizada para agrupar métodos com corpos vazios, sem implementação. Apesar de se assemelhar a uma classe abstrata, uma interface só pode conter métodos declarados, atributos e métodos padrão. A seguir, veremos um exemplo de interface:

```Java
public interface Veiculo {
    public static final String placa = "";
    public float velMax
    public void iniciar();
    public void parar();
    default void buzinar(){
      System.out.println("Buzinando");
   }
}
```

Na nossa estrutura temos:

- `interface`: É a palavra chave que diz ao Java que estamos criando uma interface. No nosso caso, a interface **Veiculo**.
- Os atributos de uma interface são por padrão `public` e `static final`. Por mais que você esqueça de inserir essas palavras-chave, a interface deixa isso implícito ao Java. E seus atributos devem ser sempre inicializados assim que declarados. 
- Os métodos da interface, `iniciar()` e `parar()` não possuem corpo - o corpo é definido pela classe que implementará essa interface.
- Os métodos da interface são por padrão `abstract` e `public`. Por mais que você esqueça de inserir essas palavras-chave, a interface deixa isso implícito ao Java.
- Antes do Java 8, só se era possível ter métodos sem implementação em interfaces. No entanto, do Java 8 em diante, agora podemos declarar métodos concretos (com implementação) usando o `default method`. Isso quer dizer que ao implementarmos uma interface, não seremos obrigados a implementar os métodos declarados como `default`, pois ele já possui uma implementação de fábrica. Um exemplo disso é o nosso método `buzinar()`.

Sozinhas, as interfaces não possuem muitas finalidades, mas elas são geralmente utilizadas em conjunto com classes, que implementam essas interfaces. Isso é possível com o uso da palavra-chave `implements`.

```Java
public class Carro implements Veiculo {
    @Override
    public void iniciar() {
        System.out.println("ligando o motor...");
    }
    @Override
    public void parar() {
        System.out.println("parando o motor...");
    }
}
```

No nosso exemplo, a classe `Carro` implementa nossa interface `Veiculo` . Por regra, quem implementa uma interface, deve também implementar todos os seus métodos sem corpo, anotados com `@Override` indicando que os métodos agora serão sobrescritos. Só não serão implementados os atributos da interface ou os `default methods`.

### Instância de uma interface

Uma interface não pode conter um método construtor, e por isso não pode ser instanciada. No entanto, há uma maneira de instanciar uma classe que implementa nossa interface e assim fazer referência a ela, como no exemplo abaixo:

```Java
// seguindo o exemplo anterior

Veiculo tesla = new Carro();

tesla.iniciar(); // ligando o motor...
```

Aqui criamos um objeto `Carro`, no entanto do tipo `Veiculo`, referenciando assim a nossa interface `Veiculo`

### Singularidades da Interface

As interfaces possuem algumas características e recursos bem interessantes, como o conceito de **herança múltipla**, onde uma classe pode implementar várias interfaces e consequentemente, os métodos que vem com elas.

```Java
public interface GPS {
    public void obterCoordenadas();
}

public interface Radio {
    public void ligarRadio();
    public void pararRadio();
}

public class Smartphone implements GPS,Radio {
    public void obterCoordenadas() {
        // retorna coordenadas
    }
    public void ligarRadio() {
      // liga o rádio
    }
    public void pararRadio() {
        // desliga o rádio
    }
}
```

Nesse exemplo, a classe Smartphone pode implementar as interfaces `GPS` e `Radio`, sempre respeitando o uso de vírgula após cada adição de uma interface, e por mais que se implemente várias, a palavra-chave `implements` só é usada uma única vez.

Outra singularidade interessante dessa estrutura é que interfaces podem herdar outras interfaces. Por exemplo:

```Java
public interface Reprodutor {
    public void iniciar();
    public void pausar();
    public void parar();
}

public interface ReprodutorMusical extends Reprodutor {
    default public void proxima() {
        System.out.println("Próxima de ReprodutorMusical");
    }
}
```

No nosso código, `Reprodutor` é nossa interface e possui métodos sem escopo e`ReprodutorMusical` é nossa segunda interface que herda de `Reprodutor`. Sendo assim, a classe que implementar `ReprodutorMusical`, implementará todos os métodos dessa interface, bem como de `Reprodutor`.

```Java
public class SmartPhone implements ReprodutorMusical {
    public void iniciar() {
        System.out.println("iniciar");
    }
    public void parar() {
        System.out.println("parar");
    }
    public void pausar() {
        System.out.println("pausar");
    }
}
```

### Classe abstrata ou Interface?

1. Classes abstratas e interfaces são ambos mecanismos importantes em Java para definir contratos e criar hierarquias de classe, mas cada um tem seu próprio propósito e casos de uso específicos. Vamos detalhar suas diferenças e quando usar cada um.

   #### Interfaces

   1. **Métodos Abstratos:** Todas os métodos dentro de uma interface são automaticamente abstratos até o Java 7, ou seja, não possuem corpo, implementação. A partir do Java 8, interfaces podem ter métodos concretos usando a palavra-chave `default`, e a partir do Java 9, métodos privados também são permitidos dentro de interfaces.
   2. **Múltipla Herança:** Java não permite que uma classe herde de várias outras classes, mas uma interface pode herdar de várias outras interfaces. Uma classe pode implementar várias interfaces, o que significa que pode adotar múltiplos contratos.
   3. **Sem Estado:** Interfaces não podem conter variáveis de instância (exceto constantes) e não podem ser instanciadas, portanto, não têm estado.
   4. **Visibilidade:** Os métodos e atributos de uma interface são, por padrão, públicos, tornando-os visíveis para todas as classes que a implementam.
   5. **Flexibilidade:** Interfaces são ideais para definir tipos que podem ser implementados por classes de diferentes hierarquias.

   **Quando usar interfaces:**

   - Quando você deseja definir um contrato que várias classes não relacionadas devem seguir.
   - Quando você precisa da flexibilidade de múltipla herança de tipo.
   - Para definir um conjunto de métodos que devem ser implementados por todas as classes que aderem à interface, independente de onde estão na hierarquia de classes.

   #### Classes Abstratas

   1. **Métodos Abstratos e Concretos:** Classes abstratas podem ter tanto métodos abstratos (sem implementação) quanto métodos concretos (com implementação).
   2. **Herança:** Uma classe pode herdar de apenas uma outra classe, mas pode implementar várias interfaces.
   3. **Estado:** Classes abstratas podem ter variáveis de instância e, portanto, podem manter estado.
   4. **Construtores:** Classes abstratas podem ter construtores, que são chamados durante a instanciação das subclasses.
   5. **Parcial Implementação:** Classes abstratas são ideais para situações onde você deseja fornecer uma implementação parcial que outras classes podem construir sobre.

   **Quando usar classes abstratas:**

   - Quando você deseja compartilhar código comum entre várias classes relacionadas.
   - Quando você precisa declarar métodos que devem ser implementados por subclasses, mas também fornecer alguma implementação comum.
   - Quando você quer manter um estado ou ter variáveis de instância compartilhadas.

   #### Diferenças e Decisão de Uso

   - **Herança Múltipla:** Use interfaces quando precisar de múltipla herança de tipo, pois uma classe pode implementar várias interfaces, mas não pode estender várias classes.
   - **Implementação Compartilhada:** Use classes abstratas quando precisar de uma implementação compartilhada entre várias classes.
   - **Flexibilidade vs. Estrutura:** Use interfaces para maior flexibilidade e quando diferentes classes não relacionadas precisarem compartilhar um contrato. Use classes abstratas para estruturas mais rigorosas onde há uma relação clara e compartilhada entre as classes.

Bem, por hoje é só. Aqui encerramos nosso tópico de Programação Orientada a Objetos. Aprendemos vários de seus elementos fundamentais, seus pilares e alguns outros recursos. Espero você na aula. Lembre-se, qualquer dúvida, não hesite em perguntar. **Até logo** 🚀!

