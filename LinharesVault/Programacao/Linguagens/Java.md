**(Notas atualizadas em 07/08/2025)**

# Iniciando
---
**IDEs recomendadas:** Intellij, Eclipse.

**JDK:** Java Development Kit (Pacote para desenvolvedores).

**JRE:** Java Runtime Enviroment (Pacote para usuários comuns que desejam executar uma aplicação java).

Para deixar claro, precisamos baixar o pacote de desenvolvimento do java (**JDK**) e alguma IDE ou editor de código.

## Processo de compilação

Atualmente é comum que diversas linguagens de programação sejam chamadas de linguagem de **alto nível**, pois sua comunicação é mais próxima da linguagem humana. Com o Java acontece o mesmo: ele é uma linguagem de alto nível que, assim como outras, precisa ser compilada para ser executada em máquinas. Nesse processo existia um problema, cada código-fonte era escrito somente para um sistema operacional ou modelo de processador,o que implicava na necessidade de escrever vários códigos para máquinas diferentes. O Java vem para quebrar isso. Ele permite que um código-fonte possa ser executado em qualquer máquina, e isso acontece através da **JVM** (Java Virtual Machine).

```
Código java (.java) --> Compilador (Javac) --> Bytecode(.class) --> JVM (Java Virtual Machine) --> CPU (execução na máquina destino)
```

Neste exemplo, o código-fonte é enviado para o compilador, o compilador, então transforma esse código em para linguagem de máquina (bytecode). Por fim, esse **bytecode** é interpretado pela JVM (Java Virtual Machine). A JVM precisa estar intalada no lado do cliente, seja por meio do **JDK** (Java Development Kit) ou do **JRE**(Java Runtime Enviroment).
# Essencial
---
## Variáveis

Java é uma linguagem estaticamente tipada, isso significa que o programador deve definir o tipo de dado para uso em variáveis e funções. Diferente de outras linguagens como Python e javascript que são dinâmicamente tipadas. Nessas, não é necessário definir os tipos de dado. 

Exemplo de alguns tipos essenciais em java:

```JAVA
//Classe para valores em textos
String nome = "Mark Grayson";

//tipos para valores inteiros e decimais
int idade = 17;
double forca = 57.03;
float velocidade = 35.00f; # valores float devem ser acompanhados por "f" ou "F"  

//tipos para valores booleanos
boolean viltrumita = true;
```

Algumas observações devem ser feitas. Primeiramente, as classes, variáveis e métodos em java devem ser definidas no padrão **camelCase** (para variáveis e métodos) ou **PascalCase** (para classes). As variáveis e métodos devem possuir a primeira letra no minúsculo. Utiliza-se letras maiúsculas, no início, somente em classes, para melhor identificação de cada coisa. Pois, podemos ter uma variável ou método com o mesmo nome da classe. 

Além disso, outra observação que devemos fazer é sobre os valores float. Eles devem ser escritos com a letra "f" ou "F" no final, pois, em java, os valores com ponto flutuante são definidos por padrão como tipo ```double```. Portanto, não podemos inserir um valor double em uma variável do tipo float, ocorre erro de compilação.

### Manipulando textos com a Classe [String]

O "tipo" **String** na verdade é uma classe em java. Diferente dos tipos primitivos, a classe String possui metodos e comportamentos internos que nos possibilitam manipular textos. Embora seja uma classe, o java oferece uma sintaxe especial para ela, permitindo a criação de um objeto da classe string de forma literal, assim como os tipos primitivos.

```java
String nome = "Peter Parker";
```

Os métodos oferecidos por essa classe são diversos. Entre eles podemos destacar alguns, eles serão utilizados de acordo com a necessidade de cada desenvolvedor. Portanto, não há a necessidade de descrever todos os métodos.

```.length()```: responsável por contar quantos caracteres existem naquela string.
```.split()```: utilizado para repartir a string em um vetor de de strings usando um delimitador de separação.
```.trim()```: remove espaços em "branco" das strings.
```.equals()```: compara uma string com outra e retorna um valor booleano.

### Conversão de valores [Type Casting]

Em Java, podemos ter dois tipos de conversão: **implícita** e **explícita**.

**Conversão implícita (Widening casting)**: Esse é o tipo de conversão mais seguro, pois o java faz o trabalho para você, sem a necessidade de um comando. Ela acontece quando queremos converter um tipo menor para um tipo maior. Sendo assim, se quisermos converter um ```int```  e armazená-lo em uma variável do tipo ```float``` , o java se encarregará de fazer a conversão. 

```java
//ENTRADA
float num1 = 4; //conversão ímplícita de int para float
System.out.println(num1)

//SAÍDA
4.0
```

**Conversão explícita (Narrowing Casting)**: Essa conversão exige que o programador faça a conversão manualmente, pois existe a possibilidade de perda de dados. Isso ocorre quando tentamos converter um tipo de dado maior em um menor. Estamos "estreitando" um tipo de dado grande para caber em um pequeno, sendo assim, podemos perder parte do seu conteúdo. Para fazer essa conversão informamos o tipo de dado para o qual queremos converter.

```java
//ENTRADA
int num2 = (int) 34.06; #conversão explícita de double para int
System.out.println(num2)

#SAÍDA
35
```

Aqui esta uma tabela sobre os tipos de dado e as conversões necessárias:

| DE \ PARA  | byte | short     | char | int       | long      | float     | double    |
| ---------- | ---- | --------- | ---- | --------- | --------- | --------- | --------- |
| **byte**   |      | Implícito | char | Implícito | Implícito | Implícito | Implícito |
| **short**  | byte |           | char | Implícito | Implícito | Implícito | Implícito |
| **char**   | byte | short     |      | Implícito | Implícito | Implícito | Implícito |
| **int**    | byte | short     | char |           | Implícito | Implícito | Implícito |
| **long**   | byte | short     | char | int       |           | Implícito | Implícito |
| **float**  | byte | short     | char | int       | long      |           | Implícito |
| **double** | byte | short     | char | int       | long      | float     |           |

### Entrada de dados
É feita com o instanciamento de uma classe. A classe **Scanner** é responsável por fazer essa coleta de dados inseridos:

```java
Scanner scan = new Scanner(System.in);

//Leituras para alguns tipos
scan.nextInt(); //tipo int
scan.nextLine(); //String
scan.nextDouble(); //Double
scan.nextFloat(); //Float
```

## Condicionais
Em java não encontramos nada especial. As estruturas condicionais são bastante similares as encontradas em outras linguagens de alto nível.

```java
//if-else padrão
if(condição){
	//bloco de código
}else if(condição){
	//bloco de código
}else{
	//bloco de código
}

//Switch case
switch(condição){
	case x:
		//bloco de código
	default:
		//bloco de código
}

//Operador ternário
condição? valor_se_verdadeiro: valor_se_falso
```

## Repetição (Loops)
Em java não encontramos nada especial. As estruturas de repetição e iteração são bastante similares as encontradas em outras linguagens de alto nível.

```java
//iteração for
for(Condição de partida; condição de chegada; valor de iteração){
	//Bloco de código
}

//iteração while
while(condição){
	//bloco de código
}

//iteração Do-while
do{
	//bloco de código
}while(condição);
```

## Interfaces

Interfaces são escopos de código que definem um grande conjunto se **métodos abstratos** (métodos sem corpo) que podem ser implementados por classes. Nas interfaces somente passamos assinatura dos métodos. Utilizamos a palavra-chave **implements** para indicar que uma interface está sendo consumida por uma classe:

```java

public interface Poderes{
   public String superVelocidade(int velocidade);
   public String SuperForca(int forca);
   public void voar();
}


public class Kriptoniano implements Poderes{

	//Atributos
	private String nome;
	private int idade;
	private String identidade;

	// setters
	public void setNome(String nome){
		this.nome = nome;
	}
	public void setIdade(int idade){
		this.idade = idade;
	}
	public void setIdentidade(String identidade){
		this.identidade = identidade;
	}

	
	@Override
	public String superVelocidade(int velociadade){
		return velocidade * 1000;
	}

	@Override
	public String superForca(int forca){
		return forca * 1000;
	}

    @Override
	public void voar(){
		System.out.println("Capacidade de voo ativada!");
	}
}
```

Uma classe tem por obrigatoriedade utilizar todos os métodos da interface que ela consome. Caso não necessite de um método, poderá fazer uma **implementação vazia** (Quando chamo um método mas não passo escopo para ele) ou **lançar uma exception** dentro do método não desejado.