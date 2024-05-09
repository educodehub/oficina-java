# Bem-vindo ao seu terceiro exercício em Java!

Neste exercício, você vai construir e rodar um programa que calcula o fatorial de um número.

## Problema

Escreva um programa que contenha a função `fatorial(num)` recebendo um natural *n* na entrada e retornando o seu fatorial **n!**. 

**Dica**: Lembre-se que o fatorial de 0 vale 1, e que não existe fatorial para números negativos (**n < 0**)!

| Como o programa deve ser |
| ------------------------ |

```
> Digite um número: 5
120

> Digite um número: -4
Entrada inválida
```

`// É isso, mãos na massa! É hora de codar!` 👨‍💻

## Instruções para construir e rodar o script

> [!TIP]
>
> Antes de criarmos o arquivo do seu terceiro exercício, contamos que você tenha um workspace padrão na sua IDE Eclipse, de preferência, a pasta `ws-eclipse` que criamos no exercício 1. Se já possuir seu workspasce definido, pode seguir com os próximos passos. 

Vamos agora criar  o projeto do seu terceiro exercício da Aula 01 de Java:

1. **Escolha do Workspace:**
   - Abra o Eclipse.
   
   - Quando solicitado, escolha uma pasta como seu Workspace. Recomendamos escolher a pasta `ws-eclipse` em `C:\Temp\` que criamos anteriormente para organizar seus projetos.
   
2. **Criação do projeto:**
   - No Eclipse, vá em `File > New > Java Project`.

   - Na janela de criação do projeto, defina o nome como **Exercicio03** e clique em `Finish`.

3. **Criação do pacote:**
- Dentro do projeto **Exercicio03**, clique com o botão direito na pasta `src`.
   
- Selecione `New > Package`.
   
- Nomeie o pacote como **application** e pressione `Enter`.

### Implementação do programa:

Agora, vamos criar o programa seguindo estas etapas:

1. **Criação da classe:**
   - Clique com o botão direito no pacote **application**.
   - Selecione `New > Class`.
   - Nomeie a classe como **Fatorial** e marque a opção `public static void main(String[] args)` antes de clicar em `Finish`.
2. **Implementação da lógica:**
   - Dentro do método `fatorial(num)`, siga as instruções do exercício no tópico [**Problema**](#Problema) para calcular o fatorial de um número natural.
   - Seu método `fatorial(num)` deve retornar um inteiro, contendo o fatorial para a entrada da função.
3. **Entrada de dados:**
   - Utilize a classe `Scanner` para ler as entradas do usuário. Importe-a adicionando `import java.util.Scanner;` no início do arquivo. Lembre-se de ao fim do seu programa, fechar o seu objeto Scanner, da forma que ensinamos na aula.
4. **Exibição dos resultados:**
   - Utilize `System.out.println()` para exibir o retorno da sua função `fatorial(num)`.

### Como rodar o programa:

Para executar o programa e ver os resultados, siga estas instruções:

1. **Compilação do código:**
   - Após terminar de escrever o código, salve o arquivo.
   - Clique com o botão direito no arquivo **Fatorial.java** no Package Explorer.
   - Selecione `Run As > Java Application` para compilar e executar o programa.
2. **Entrada dos dados:**
   - Insira um número natural *n* conforme solicitado pelo programa.
3. **Visualização dos resultados:**
   - Verifique se o resultado do fatorial foi exibido corretamente e se o resultado é verdadeiro. Observe como deve ser a saída do seu programa de acordo com o tópico [**Problema**](#Problema) em **Como o programa deve ser**.

## Como enviar?

Acesse o link do [Exercício 03 - Oficina de Java - Aula 1](https://classroom.google.com/c/Njc1ODQ4MTQxMjk5/a/NjgyODI2MTQ5NTQ2/details) e você será redirecionado para a sua atividade no Classroom. Lá conterão as instruções para que submeta seu trabalho **Fatorial.java**. 

**Boa sorte!!! Nos vemos no próximo exercício** 👋

