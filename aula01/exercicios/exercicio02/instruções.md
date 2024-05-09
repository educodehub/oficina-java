# Bem-vindo ao seu segundo exercício em Java!

Neste exercício, você vai construir e rodar um programa que imprime a tabuada de um número inserido pelo usuário.

## Problema

Escreva um programa que solicita ao usuário um número e imprime a tabuada desse número de 1 a 10.

**Dica**: Utilize um loop `for` para percorrer os números de 1 a 10 e imprima o resultado da multiplicação do número inserido pelo usuário pelo número do loop.

| Como o programa deve ser |
| ------------------------ |

```
> Digite um número para a tabuada: 5
Tabuada de 5:
5 x 1 = 5
5 x 2 = 10
5 x 3 = 15
5 x 4 = 20
5 x 5 = 25
5 x 6 = 30
5 x 7 = 35
5 x 8 = 40
5 x 9 = 45
5 x 10 = 50
```

`// É isso, mãos na massa! É hora de codar!` 👨‍💻

## Instruções para construir e rodar o script

> [!TIP]
>
> Antes de criarmos o arquivo do seu segundo exercício, contamos que você tenha um workspace padrão na sua IDE Eclipse, de preferência, a pasta `ws-eclipse` que criamos no exercício anterior. Se já possuir seu workspasce definido, pode seguir com os próximos passos. 

Vamos agora criar o programa do seu segundo exercício da Aula 01 de Java:

1. **Escolha do Workspace:**
   - Abra o Eclipse.

   - Quando solicitado, escolha uma pasta como seu Workspace. Recomendamos escolher a pasta `ws-eclipse` em `C:\Temp\` que criamos anteriormente para organizar seus projetos.
2. **Criação do projeto:**
   - No Eclipse, vá em `File > New > Java Project`.

   - Na janela de criação do projeto, defina o nome como **Exercicio02** e clique em `Finish`.
3. **Criação do pacote:**
   - Dentro do projeto **Exercicio02**, clique com o botão direito na pasta `src`.

   - Selecione `New > Package`.

   - Nomeie o pacote como **application** e pressione `Enter`.

### Implementação do programa:

Agora, vamos criar o programa seguindo estas etapas:

1. **Criação da classe:**
   - Clique com o botão direito no pacote **application**.
   - Selecione `New > Class`.
   - Nomeie a classe como **Tabuada** e marque a opção `public static void main(String[] args)` antes de clicar em `Finish`.
2. **Implementação da lógica:**
   - Dentro do método `main`, siga as instruções do exercício no tópico [**Problema**](#Problema) para receber corretamente as entradas do usuário e construir a tabuada do número em questão.
3. **Entrada de dados:**
   - Utilize a classe `Scanner` para ler as entradas do usuário. Importe-a adicionando `import java.util.Scanner;` no início do arquivo. Lembre-se de ao fim do seu programa, fechar o seu objeto Scanner, da forma que ensinamos na aula.
4. **Exibição dos resultados:**
   - Utilize `System.out.println()` para exibir a tabuada formatada de acordo com o exibido no no tópico [**Problema**](#Problema) em **Como o programa deve ser**.

## Como enviar?

Acesse o link do [Exercício 02 - Oficina de Java - Aula 1](https://classroom.google.com/c/Njc1ODQ4MTQxMjk5/a/NjgyOTgyNDY2NTY3/details) e você será redirecionado para a sua atividade no Classroom. Lá conterão as instruções para que submeta seu trabalho **Tabuada.java**.

**Boa sorte! Nos vemos no próximo exercício!** 👋