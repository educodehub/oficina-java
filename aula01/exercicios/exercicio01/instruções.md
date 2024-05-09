# Bem-vindo ao seu primeiro exercício em Java!

Neste exercício, iremos construir e rodar um programa que calcula a área e o valor por metros quadrados de um terreno.

## Problema

Faça um programa que leia as medidas da largura e comprimento de um terreno retangular, bem como o valor do metro quadrado do terreno. Em seguida, o programa deve mostrar o valor da área do terreno, bem como o valor do preço do terreno, ambos com duas casas decimais.

**Dica:** Lembre-se que a fórmula da área de um retângulo é *A=b⋅ h*.

| Como o programa deve ser |
| ------------------------ |

```
> Largura: 12.0
> Comprimento: 20.0
> Valor do metro²: 100.00
 
AREA = 300.00
PRECO = 24000.00
```

`// É isso, mãos na massa! É hora de codar!` 👨‍💻

## Instruções para construir e rodar o script

> [!TIP]
>
> Antes de criarmos o arquivo do seu primeiro exercício, é importante que crie uma pasta destinada a guardar todos os seus programas e futuros projetos. Recomendamos que crie a pasta `ws-eclipse` no diretório `C:\Temp\`. Ao criar abra o seu eclipse e use a pasta que criou como **workspace** (área de trabalho). Isso irá ajudar a organizar todos os seu arquivos de exercícios desta oficina.

Vamos agora seguir alguns passos para criarmos o projeto do seu primeiro exercício da Aula 01 de Java:

1. **Escolha do Workspace:**

   - Abra o Eclipse.

   - Quando solicitado, escolha ou crie uma pasta como seu Workspace. Recomendamos escolher a pasta `ws-eclipse` em `C:\Temp\` que criamos anteriormente para organizar seus projetos.

4. **Criação do projeto:**

   - No Eclipse, vá em `File > New > Java Project`.

   -  Na janela de criação do projeto, defina o nome como **Exercicio01** e clique em `Finish`.

7. **Criação do pacote:**

   - Dentro do projeto **Exercicio01**, clique com o botão direito na pasta `src`.

   - Selecione `New > Package`.

   - Nomeie o pacote como **application** e pressione `Enter`.

### Implementação do programa:

Agora, vamos criar o programa seguindo estas etapas:

1. **Criação da classe:**
   - Clique com o botão direito no pacote **application**.
   - Selecione `New > Class`.
   - Nomeie a classe como **Area** e marque a opção `public static void main(String[] args)` antes de clicar em `Finish`.
2. **Implementação da lógica:**
   - Dentro do método `main()`, siga as instruções do exercício que se encontram no tópico [**Problema**](#Problema) para calcular a área e o preço do terreno.
3. **Entrada de dados:**
   - Utilize a classe `Scanner` para ler as entradas do usuário. Importe-a adicionando `import java.util.Scanner;` no início do arquivo. Lembre-se de ao fim do seu programa, fechar o seu objeto Scanner, da forma que ensinamos na aula.
4. **Exibição dos resultados:**
   - Utilize `System.out.printf()` para exibir a área e o preço do terreno com duas casas decimais formatados como definimos no tópico [**Problema**](#Problema) em **Como o programa deve ser**.

### Como rodar o programa:

Para executar o programa e ver os resultados, siga estas instruções:

1. **Compilação do código:**
   - Após terminar de escrever o código, salve o arquivo.
   - Clique com o botão direito no arquivo **Area.java** no Package Explorer.
   - Selecione `Run As > Java Application` para compilar e executar o programa.
2. **Entrada dos dados:**
   - Insira a largura, o comprimento e o valor do metro quadrado do terreno conforme solicitado pelo programa.
3. **Visualização dos resultados:**
   - Verifique se a área e o preço do terreno foram exibidos corretamente, seguindo o formato especificado no tópico tópico [**Problema**](#Problema) em **Como o programa deve ser**.

## Como enviar?

Acesse o link do [Exercício 01 - Oficina de Java - Aula 1](https://classroom.google.com/c/Njc1ODQ4MTQxMjk5/a/NjgyNzg3ODE1MjU1/details) e você será redirecionado para a sua atividade no Classroom. Lá conterão as instruções para que submeta seu trabalho **Area.java**. 

**Boa sorte!!! Nos vemos no próximo exercício** 👋