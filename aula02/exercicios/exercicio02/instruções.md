# Bem-vindo ao seu quinto exercício em Java!

Neste exercício, você vai construir e rodar um programa que testa os principais métodos de manipulação de Strings que vimos na Aula 02.

## Problema

Escreva um programa que contenha um frase definida anteriormente, de preferência com mais de cinco palavras, e utilize os métodos `toLowerCase(), toUpperCase(), trim(), substring() e replace()` para manipular essa entrada de dados. Mais instruções se encontram no tópico [Implementação do programa](##Implementação-do-programa) em **Implementação da lógica**.

| Como o programa deve ser |
| ------------------------ |

```shell
Frase original: " Hoje é um Belo Dia  "
Em minúsculas: "hoje é um belo dia"
Em maiúsculas: "HOJE É UM BELO DIA"
Sem espaços em branco: "Hoje é um Belo Dia"
Substring: "um Belo Dia"
Substituição: "Hoje é um Maravilhoso Dia"
```

`// É isso, mãos na massa! É hora de codar!` 👨‍💻

## Instruções para construir e rodar o script

> [!TIP]
>
> Antes de criarmos o arquivo do seu quinto exercício, contamos que você tenha um workspace padrão na sua IDE Eclipse, de preferência, a pasta `ws-eclipse` que criamos no exercício 1. Se já possuir seu workspasce definido, pode seguir com os próximos passos. 

Vamos agora criar  o projeto do seu quinto exercício da Aula 02 de Java:

1. **Escolha do Workspace:**
   - Abra o Eclipse.
   
   - Quando solicitado, escolha uma pasta como seu Workspace. Recomendamos escolher a pasta `ws-eclipse` em `C:\Temp\` que criamos anteriormente para organizar seus projetos.
   
2. **Criação do projeto:**
   - No Eclipse, vá em `File > New > Java Project`.

   - Na janela de criação do projeto, defina o nome como **Exercicio05** e clique em `Finish`.

3. **Criação do pacote:**

   - Dentro do projeto **Exercicio05**, clique com o botão direito na pasta `src`.
     
   - Selecione `New > Package`.
     
   - Nomeie o pacote como **application** e pressione `Enter`.

### Implementação do programa:

Agora, vamos criar o programa seguindo estas etapas:

1. **Criação da classe:**
   - Clique com o botão direito no pacote **application**.
   - Selecione `New > Class`.
   - Nomeie a classe como **Strings** e marque a opção `public static void main(String[] args)` antes de clicar em `Finish`.
2. **Implementação da lógica:**
   - Dentro do método `main()`, siga as instruções do exercício no tópico [**Problema**](#Problema) para criar o seu programa
   - Para converter a String em minúsculas e maiúsculas, utilize os métodos `toLowerCase() e toUpperCase()`
   - Para remover os espaços, lembre-se do método `trim()` e o seu uso.
   - Ao usar o método `substring()`, use como parâmetro de início, o valor **7**, e como parâmetro de fim, o valor **18**. Por isso sua frase deve ser grande o suficiente, para que o programa consiga extrair uma substring com esses valores.
   - Utilize o método `replace()` para executar a substituição dentro da String.
3. **Entrada de dados:**
   - Dessa vez você irá definir a sua entrada de dados dentro do próprio programa, apenas por questões didáticas e da melhor execução do seu script.
4. **Exibição dos resultados:**
   - Utilize `System.out.println()` para exibir as saídas do seu programa de acordo com o tópico [**Problema**](#Problema) em **Como o programa deve ser**

### Como rodar o programa:

Para executar o programa e ver os resultados, siga estas instruções:

1. **Compilação do código:**
   - Após terminar de escrever o código, salve o arquivo.
   - Clique com o botão direito no arquivo **Strings.java** no Package Explorer.
   - Selecione `Run As > Java Application` para compilar e executar o programa.
3. **Visualização dos resultados:**
   - Verifique se o resultado do programa foi exibido corretamente e se o resultado é verdadeiro. Observe como deve ser a saída do seu programa de acordo com o tópico [**Problema**](#Problema) em **Como o programa deve ser**.

## Como enviar?

Acesse o link do [Exercício 05 - Oficina de Java - Aula 2](https://classroom.google.com/c/Njc1ODQ4MTQxMjk5/a/NjgzOTk5ODE5NzAz/details) e você será redirecionado para a sua atividade no Classroom. Lá conterão as instruções para que submeta seu trabalho **Strings.java**. 

**Boa sorte!!! Nos vemos no próximo exercício** 👋

