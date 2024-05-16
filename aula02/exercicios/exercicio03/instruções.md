# Bem-vindo ao seu sexto exercício em Java!

Neste exercício, você vai construir e rodar um programa para praticar a criação e chamada de métodos em Java.

## Problema

Escreva um programa que declare três métodos diferentes que operam em arrays de inteiros. Os métodos são: um para calcular a média dos valores de um vetor, um para verificar o maior elemento deste vetor, e um último para contar quantos valores pares há neste array. Lembre-se que os três métodos devem estar inclusos na mesma classe do seu método `main()`. Para detalhes mais específicos, vá para o tópico [Implementação do programa](##Implementação-do-programa) em **Implementação da lógica**. Por exemplo, para o array **`Array: [5, 12, 8, 20, 15]`** a saída deveria ser essa:

| Como o programa deve ser |
| ------------------------ |

```shell
Média dos valores: 12
Maior valor: 20
Número de valores pares: 3
```

`// É isso, mãos na massa! É hora de codar!` 👨‍💻

## Instruções para construir e rodar o script

> [!TIP]
>
> Antes de criarmos o arquivo do seu quarto exercício, contamos que você tenha um workspace padrão na sua IDE Eclipse, de preferência, a pasta `ws-eclipse` que criamos no exercício 1. Se já possuir seu workspasce definido, pode seguir com os próximos passos. 

Vamos agora criar  o projeto do seu sexto exercício da Aula 02 de Java:

1. **Escolha do Workspace:**
   - Abra o Eclipse.
   
   - Quando solicitado, escolha uma pasta como seu Workspace. Recomendamos escolher a pasta `ws-eclipse` em `C:\Temp\` que criamos anteriormente para organizar seus projetos.
   
2. **Criação do projeto:**
   - No Eclipse, vá em `File > New > Java Project`.

   - Na janela de criação do projeto, defina o nome como **Exercicio06** e clique em `Finish`.

3. **Criação do pacote:**

   - Dentro do projeto **Exercicio06**, clique com o botão direito na pasta `src`.
     
   - Selecione `New > Package`.
     
   - Nomeie o pacote como **application** e pressione `Enter`.

### Implementação do programa:

Agora, vamos criar o programa seguindo estas etapas:

1. **Criação da classe:**
   - Clique com o botão direito no pacote **application**.
   - Selecione `New > Class`.
   - Nomeie a classe como **Metodos** e marque a opção `public static void main(String[] args)` antes de clicar em `Finish`.
2. **Implementação da lógica:**
   - Dentro da sua classe **Metodos** você irá declarar e implementar os três métodos que o exercício pede: `calcularMedia(), maiorValor() e contarPares()`. Lembre-se que ainda dentro da sua classe **Metodos** você deve possuir o método principal `main()`;
   - O seu método `calcularMedia()` deve receber como parâmetro um vetor de inteiro e executar a lógica para iterar sobre esse vetor e retornar a média dos elementos contidos no array.
   - O método `maiorValor()` também deve receber como entrada um vetor de inteiros, e dentro do escopo do seu método, retornar o maior elemento contido neste vetor.
   - Por fim, o `contarPares()` , da mesma forma que os outros métodos, deve receber um vetor de inteiros e retornar a quantidade de números pares dentro deste vetor.
   - Use o laço `for` para percorrer o seu array e executar a lógica específica de cada método.
   - Defina seu vetor no método `main()`, declarando o comprimento e valores do vetor diretamente na sua inicialização
3. **Entrada de dados:**
   - Dessa vez você irá definir a sua entrada de dados dentro do próprio programa, mais especificamente dentro do seu vetor.
4. **Exibição dos resultados:**
   - Utilize `System.out.println()` para exibir as saídas do seu programa de acordo com o tópico [**Problema**](#Problema) em **Como o programa deve ser**

### Como rodar o programa:

Para executar o programa e ver os resultados, siga estas instruções:

1. **Compilação do código:**
   - Após terminar de escrever o código, salve o arquivo.
   - Clique com o botão direito no arquivo **Metodos.java** no Package Explorer.
   - Selecione `Run As > Java Application` para compilar e executar o programa.
3. **Visualização dos resultados:**
   - Verifique se o resultado do programa foi exibido corretamente e se o resultado é verdadeiro. Observe como deve ser a saída do seu programa de acordo com o tópico [**Problema**](#Problema) em **Como o programa deve ser**.

## Como enviar?

Acesse o link do [Exercício 06 - Oficina de Java - Aula 2](https://classroom.google.com/c/Njc1ODQ4MTQxMjk5/a/Njg0MTU1MTczMDQz/details) e você será redirecionado para a sua atividade no Classroom. Lá conterão as instruções para que submeta seu trabalho **Metodos.java**. 

**Boa sorte!!! Nos vemos no próximo exercício** 👋

