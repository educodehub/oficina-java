# Bem-vindo ao seu nono exercício em Java!

Neste exercício, você vai construir e rodar um programa de uma conta bancária, simulando transações de depósito e saque, bem como o cadastro de uma nova conta.

## Problema

Em um banco, para se cadastrar uma conta bancária, é necessário informar o número da conta, o nome do titular da conta e o valor de depósito inicial. Este valor de depósito inicial, entretanto, é opcional, ou seja: se o titular não tiver dinheiro a depositar no momento de abrir a sua conta, o depósito inicial não será feito e o saldo inicial da conta será, naturalmente, zero.

**Importante**: Uma vez que a conta foi aberta, o número da conta não poderá ser alterado. Lembre-se dos conceitos e recursos de encapsulamento.

Por fim, o saldo e nome do titular podem ser alterados livremente. No entanto, o saldo só deve aumentar mediante depósito e diminuir caso haja um saque. Para cada saque realizado, o banco cobra uma taxa de R$ 5.00. 

**Nota**: A conta pode ficar com saldo negativo se o saldo não for suficiente pra realizar o saque e/ou pagar a taxa.

Sua missão é fazer um programa que realize o cadastro de uma conta, dando a opção para que seja ou não informado o valor do depósito inicial. Em seguida, realizar um depósito e depois um saque, sempre mostrando os dados da conta após cada operação.

| Como o programa deve ser |
| ------------------------ |

```shell
> Número da conta: 8729
> Titular da conta: Max Newbar
> Deseja faze um depósito inicial (y/n)? y
> Entre com o valor do depósito inicial: 500,00

Dados da conta:
Conta 8729, Titular: Max Newbar, Saldo: 500,00

Entre com o valor de depósito: 200,00
Dados atualizados:
Conta 8729, Titular: Max Newbar, Saldo: 700,00

Entre com o valor de saque: 300,00
Dados atualizados:
Conta 8729, Titular: Max Newbar, Saldo: 395,00
```

`// É isso, mãos na massa! É hora de codar!` 👨‍💻

## Instruções para construir e rodar o script

> [!TIP]
>
> Antes de criarmos o arquivo do seu nono exercício, contamos que você tenha um workspace padrão na sua IDE Eclipse, de preferência, a pasta `ws-eclipse` que criamos no exercício 1. Se já possuir seu workspasce definido, pode seguir com os próximos passos. 

Vamos agora criar  o projeto do seu nono exercício da Aula 03 de Java:

1. **Escolha do Workspace:**
   - Abra o Eclipse.
   
   - Quando solicitado, escolha uma pasta como seu Workspace. Recomendamos escolher a pasta `ws-eclipse` em `C:\Temp\` que criamos anteriormente para organizar seus projetos.
   
2. **Criação do projeto:**
   - No Eclipse, vá em `File > New > Java Project`.

   - Na janela de criação do projeto, defina o nome como **Exercicio09** e clique em `Finish`.

3. **Criação do pacote:**

   - Dentro do projeto **Exercicio09**, clique com o botão direito na pasta `src`.
     
   - Selecione `New > Package`.
     
   - Nomeie o pacote como **application** e pressione `Enter`.

### Implementação do programa:

Agora, vamos criar o programa seguindo estas etapas:

1. **Criação da classe:**
   - Clique com o botão direito no pacote **application**.
   - Selecione `New > Class`.
   - Nomeie a classe como **ContaBanco ** e clique em `Finish`
   - Novamente, clique com o botão direito no pacote **application**.
   - Selecione `New > Class`.
   - Nomeie a classe como **Program** e marque a opção `public static void main(String[] args)` antes de clicar em `Finish`.
2. **Implementação da lógica:**
   - Dentro da sua classe **ContaBanco** é onde você vai inserir toda a lógica de cadastro de uma nova conta bancária, bem como as operações de depósito e saque.
   - Lembre-se de usar os métodos acessores e de definir seus atributos como `private`.
   - Implemente construtores padrão e parametrizado.
   - No seu método de depósito, implemente toda a lógica para esta ação. O mesmo vale para o saque. Lembre-se que se a quantia de saque for maior do que o saldo da conta, resulta numa operação inválida. No entanto, se o dinheiro for suficiente, o saque pode ser realizado, mesmo que a conta fique no vermelho por pagar taxa de R$ 5.00 em cada saque.
   - Dentro da sua classe **Program** você deve implementar toda a lógica de criação do objeto **ContaBanco** bem como a verificação de um possível depósito inicial.
3. **Entrada de dados:**
   - A sua entrada de dados deve ser feita usando o `Scanner` na classe **Program**.
   - Os dados recebidos serão usados para inicializar o seu objeto `ContaBanco`.
4. **Exibição dos resultados:**
   - Utilize o método `toString()` da sua classe **ContaBanco** para exibir as informações em formato de String.
   - Na sua classe **Program** chame esse método usando o objeto `ContaBanco` criado para exibir as informações na tela conforme o tópico [**Problema**](##Problema) em **Como o programa deve ser**.

### Como rodar o programa:

Para executar o programa e ver os resultados, siga estas instruções:

1. **Compilação do código:**
   - Após terminar de escrever o código, salve o arquivo.
   - Clique com o botão direito no arquivo **Program.java** no Package Explorer.
   - Selecione `Run As > Java Application` para compilar e executar o programa.
3. **Visualização dos resultados:**
   - Verifique se o resultado do programa foi exibido corretamente. Observe como deve ser a saída do seu programa de acordo com o tópico [**Problema**](#Problema) em **Como o programa deve ser**.

## Como enviar?

Acesse o link do [Exercício 09 - Oficina de Java - Aula 3](https://classroom.google.com/c/Njc1ODQ4MTQxMjk5/a/NjkzMDM0ODEyNjU5/details) e você será redirecionado para a sua atividade no Classroom. Lá conterão as instruções para que submeta seu trabalho **ContaBanco.java** e **Program.java**.

**Boa sorte!!! Nos vemos no próximo exercício** 👋

