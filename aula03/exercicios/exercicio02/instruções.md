# Bem-vindo ao seu oitavo exercício em Java!

Neste exercício, você vai criar e rodar um programa de base de dados de funcionários, testando seus conhecimentos de encapsulamento e criação de métodos em POO

## Problema

Você foi desafiado a desenvolver um programa que lê dados de um funcionário (**nome, salário bruto e taxa de imposto**) e em seguida mostrar os dados do seu nome e salário líquido (**valor real depois de aplicada a taxa de imposto**). Seu programa deve ainda, em sequência, aumentar o valor do funcionário com base em uma porcentagem (**somente o salário bruto é afetado pela porcentagem**), e exibir os dados atualizados desse funcionário.

Seu objetivo é desenvolver um programa para gerenciar os dados de um funcionário, calcular seu salário líquido e aplicar um aumento salarial com base em uma porcentagem fornecida.

| Como o programa deve ser |
| ------------------------ |

```
> Entre com os dados do funcionário:
> Nome: João da Silva
> Salário Bruto: 3000.00
> Imposto: 250.00

> Funcionário: João da Silva Salário, 2750.00

> Entre com a porcentagem de aumento do salário: 10

> Dados atualizados do funcionário: João da Silva, 3050.00
```

`// É isso, mãos na massa! É hora de codar!` 👨‍💻

> [!TIP] 
>
> Antes de criarmos o arquivo do seu oitavo exercício, contamos que você tenha um workspace padrão na sua IDE Eclipse, de preferência, a pasta `ws-eclipse` que criamos no exercício 1. Se já possuir seu workspasce definido, pode seguir com os próximos passos.

Vamos agora criar  o projeto do seu oitavo exercício da Aula 03 de Java:

1. **Escolha do Workspace:**
   - Abra o Eclipse.

   - Quando solicitado, escolha uma pasta como seu Workspace. Recomendamos escolher a pasta `ws-eclipse` em `C:\Temp\` que criamos anteriormente para organizar seus projetos.

2. **Criação do projeto:**
   - No Eclipse, vá em `File > New > Java Project`.

   - Na janela de criação do projeto, defina o nome como **Exercicio08** e clique em `Finish`.

3. **Criação do pacote:**

   - Dentro do projeto **Exercicio08**, clique com o botão direito na pasta `src`.

   - Selecione `New > Package`.

   - Nomeie o pacote como **application** e pressione `Enter`.

### Implementação do programa:

Agora, vamos criar o programa seguindo estas etapas:

1. **Criação da classe:**
   - Clique com o botão direito no pacote **application**.
   - Selecione `New > Class`.
   - Nomeie a classe como **Funcionario** e clique em `Finish`.
   - Novamente, clique com o botão direito no pacote **application**.
   - Selecione `New > Class`.
   - Nomeie a classe como **Program** e marque a opção `public static void main(String[] args)` antes de clicar em `Finish`.
2. **Implementação da lógica:**
   - Dentro da sua classe **Funcionario** é onde ficará toda a sua lógica de desenvolvimento dessa classe, desde a criação dos atributos até os métodos que irão manipular essas propriedades.
   - Lembre-se de usar o conceito de **encapsulamento** visto na Aula 03 de Introdução a POO.
   - Defina bem os seus atributos, conforme apresentado no tópico [**Problema**](##Problema), e implemente corretamente os métodos que se pede. Método para o cálculo do imposto e para o aumento do salário
   - Na sua classe **Program** é onde conterá a lógica da criação de um novo objeto e da inicialização deste usando os dados recebidos do usuário.
   - Você pode inicializar um novo objeto **Funcionario** usando um construtor parametrizado ou os métodos `setters`, fica ao seu critério.
3. **Entrada de dados:**
   - A sua entrada de dados deve ser feita utilizando a classe `Scanner`, implementada na classe **Program** do seu projeto.
4. **Exibição dos resultados:**
   - Utilize `System.out.println()` e `System.out.print()` para exibir as saídas do seu programa de acordo com o tópico [**Problema**](#Problema) em **Como o programa deve ser**. 
   - Utilize esse método de saída de dados juntamente com os métodos `getters` da sua classe **Funcionario** para buscar o valor de um atributo.

### Como rodar o programa:

Para executar o programa e ver os resultados, siga estas instruções:

1. **Compilação do código:**
   - Após terminar de escrever o código, salve o arquivo.
   - Clique com o botão direito no arquivo **Program.java** no Package Explorer.
   - Selecione `Run As > Java Application` para compilar e executar o programa.
2. **Visualização dos resultados:**
   - Verifique se o resultado do programa foi exibido corretamente. Observe como deve ser a saída do seu programa de acordo com o tópico [**Problema**](#Problema) em **Como o programa deve ser**.

## Como enviar?

Acesse o link do [Exercício 08 - Oficina de Java - Aula 3](https://classroom.google.com/c/Njc1ODQ4MTQxMjk5/a/NjkzMDM0MzU4NDI5/details) e você será redirecionado para a sua atividade no Classroom. Lá conterão as instruções para que submeta seu trabalho **Funcionario.java** e **Program.java**.

**Boa sorte!!! Nos vemos no próximo exercício** 👋



