# Bem-vindo ao seu quarto exercício em Java!

Neste exercício, você vai construir e rodar um programa que exibe um vetor e o cálculo  da soma dos seus elementos

## Problema

Escreva um programa que declare e inicialize um array unidimensional (vetor) de inteiros com tamanho **5**. Seu programa deve primeiramente printar o vetor criado na sua forma original, em seguida exibir cada elemento desse vetor em uma única linha, separados por espaço, e por fim, exibir a soma dos itens desse array.

**Dica**: Use a função `Array.toString()` para converter seu array para uma String printável.

| Como o programa deve ser |
| ------------------------ |

```shell
Array: [3, 12, 8, 5, 10]
Elementos do array: 3 12 8 5 10
Soma dos elementos: 38
```

`// É isso, mãos na massa! É hora de codar!` 👨‍💻

## Instruções para construir e rodar o script

> [!TIP]
>
> Antes de criarmos o arquivo do seu quarto exercício, contamos que você tenha um workspace padrão na sua IDE Eclipse, de preferência, a pasta `ws-eclipse` que criamos no exercício 1. Se já possuir seu workspasce definido, pode seguir com os próximos passos. 

Vamos agora criar  o projeto do seu quarto exercício da Aula 02 de Java:

1. **Escolha do Workspace:**
   - Abra o Eclipse.
   
   - Quando solicitado, escolha uma pasta como seu Workspace. Recomendamos escolher a pasta `ws-eclipse` em `C:\Temp\` que criamos anteriormente para organizar seus projetos.
   
2. **Criação do projeto:**
   - No Eclipse, vá em `File > New > Java Project`.

   - Na janela de criação do projeto, defina o nome como **Exercicio04** e clique em `Finish`.

3. **Criação do pacote:**

   - Dentro do projeto **Exercicio04**, clique com o botão direito na pasta `src`.
     
   - Selecione `New > Package`.
     
   - Nomeie o pacote como **application** e pressione `Enter`.

### Implementação do programa:

Agora, vamos criar o programa seguindo estas etapas:

1. **Criação da classe:**
   - Clique com o botão direito no pacote **application**.
   - Selecione `New > Class`.
   - Nomeie a classe como **Vetor** e marque a opção `public static void main(String[] args)` antes de clicar em `Finish`.
2. **Implementação da lógica:**
   - Dentro do método `main()`, siga as instruções do exercício no tópico [**Problema**](#Problema) para criar o seu vetor.
   - Para tornar o seu vetor uma String printável, use a função `Array.toString()` e exiba os elementos do vetor conforme a primeira linha do tópico [**Problema**](#Problema) em **Como o programa deve ser**.
   - Use o laço `for` para percorrer o seu vetor e exibir cada elemento separadamente, além de realizar o cálculo de soma entre eles.
3. **Entrada de dados:**
   - Dessa vez você irá definir a sua entrada de dados dentro do próprio programa, mais especificamente dentro do seu vetor.
4. **Exibição dos resultados:**
   - Utilize `System.out.println()` e `System.out.print()` para exibir as saídas do seu programa de acordo com o tópico [**Problema**](#Problema) em **Como o programa deve ser**

### Como rodar o programa:

Para executar o programa e ver os resultados, siga estas instruções:

1. **Compilação do código:**
   - Após terminar de escrever o código, salve o arquivo.
   - Clique com o botão direito no arquivo **Vetor.java** no Package Explorer.
   - Selecione `Run As > Java Application` para compilar e executar o programa.
3. **Visualização dos resultados:**
   - Verifique se o resultado do programa foi exibido corretamente e se o resultado é verdadeiro. Observe como deve ser a saída do seu programa de acordo com o tópico [**Problema**](#Problema) em **Como o programa deve ser**.

## Como enviar?

Acesse o link do [Exercício 04 - Oficina de Java - Aula 2](https://classroom.google.com/c/Njc1ODQ4MTQxMjk5/a/NjgzOTk2ODI5MDYx/details) e você será redirecionado para a sua atividade no Classroom. Lá conterão as instruções para que submeta seu trabalho **Vetor.java**. 

**Boa sorte!!! Nos vemos no próximo exercício** 👋

