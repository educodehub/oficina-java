# Bem-vindo ao seu sétimo exercício em Java!

Neste exercício, você vai construir um programa para treinar a criação de classes, objetos e métodos. Elementos fundamentais da Programação Orientada a Objetos.

## Problema

Você foi chamado para desenvolver o sistema de cadastro de uma biblioteca. Seu trabalho é simples: você precisa implementar um programa que cadastre novos livros, recebendo seus nomes, autores e ano de publicação. Você deve receber esses dados de entrada através do usuário, que será a bibliotecária, e a cada novo cadastro, as informações do livro precisam ser exibidas em tela, questões de controle.


| Como o programa deve ser |
| ------------------------ |

```
> Entre com os dados do livro:
> Título: The Great Gatsby
> Author: F. Scott Fitzgerald
> Year: 1925

> Dados do livro:
The Great Gatsby, F. Scott Fitzgeral, 1925.

```

`// É isso, mãos na massa! É hora de codar!` 👨‍💻


> [!TIP]
>
> Antes de criarmos o arquivo do seu sétimo exercício, contamos que você tenha um workspace padrão na sua IDE Eclipse, de preferência, a pasta `ws-eclipse` que criamos no exercício 1. Se já possuir seu workspasce definido, pode seguir com os próximos passos. 

Vamos agora criar  o projeto do seu sétimo exercício da Aula 03 de Java:

1. **Escolha do Workspace:**
   - Abra o Eclipse.

   - Quando solicitado, escolha uma pasta como seu Workspace. Recomendamos escolher a pasta `ws-eclipse` em `C:\Temp\` que criamos anteriormente para organizar seus projetos.

2. **Criação do projeto:**
   - No Eclipse, vá em `File > New > Java Project`.

   - Na janela de criação do projeto, defina o nome como **Exercicio07** e clique em `Finish`.

3. **Criação do pacote:**

   - Dentro do projeto **Exercicio07**, clique com o botão direito na pasta `src`.

   - Selecione `New > Package`.

   - Nomeie o pacote como **application** e pressione `Enter`.

### Implementação do programa:

Agora, vamos criar o programa seguindo estas etapas:

1. **Criação da classe:**
   - Clique com o botão direito no pacote **application**.
   - Selecione `New > Class`.
   - Nomeie a classe como **Livro** e clique em `Finish`.
   - Clique novamente no pacote **application** com o botão direito.
   - Selecione `New > Class`.
   - Nomeie a classe como **Program** e marque a opção `public static void main(String[] args)` antes de clicar em `Finish`.
2. **Implementação da lógica:**
   - Dentro da sua classe **Livro**, crie os atributos `nome, autor e anoDePublicacao`. 
   - Ainda nessa classe, lembre-se de implementar o construtor, métodos acessores e o método `toString()` para exibir uma saída visual dos dados do seu objeto.
   - Já na sua classe **Program** você deve implementar a lógica da criação de um objeto `Livro` e exibir as informações desse objeto na tela.
3. **Entrada de dados:**
   - Utilize a classe `Scanner` para receber dados do usuário.
   - Para inserir as informações advindas do usuário, crie seu objeto `Livro` usando um construtor parametrizado.
4. **Exibição dos resultados:**
   - Utilize o método `toString()` da sua classe **Livro** para exibir as informações do objeto conforme mostrado no tópico [**Problema**](##Problema) em **Como o programa deve ser**.

### Como rodar o programa:

Para executar o programa e ver os resultados, siga estas instruções:

1. **Compilação do código:**
   - Após terminar de escrever o código, salve o arquivo.
   - Clique com o botão direito no arquivo **Program.java** no Package Explorer.
   - Selecione `Run As > Java Application` para compilar e executar o programa.
2. **Visualização dos resultados:**
   - Verifique se o resultado do programa foi exibido corretamente. Observe como deve ser a saída do seu programa de acordo com o tópico [**Problema**](#Problema) em **Como o programa deve ser**.

## Como enviar?

Acesse o link do [Exercício 07 - Oficina de Java - Aula 3](https://classroom.google.com/c/Njc1ODQ4MTQxMjk5/a/NjkzMDMxMzU1NTEz/details) e você será redirecionado para a sua atividade no Classroom. Lá conterão as instruções para que submeta seu trabalho **Livro.java** e **Program.java**. 

**Boa sorte!!! Nos vemos no próximo exercício** 👋