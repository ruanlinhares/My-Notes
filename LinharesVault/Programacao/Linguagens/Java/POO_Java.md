**(Notas atualizadas em 22/07/2025)**

# Iniciando
---
**Programação orientada a objeto (POO)** é um paradigma usado por algumas linguagens como o java. Ela surge para encapsular, e assim, organizar código em torno de objetos em vez de funções ou lógica. **POO** visa modelar o mundo real  dentro do código, representando entidades como objetos que possuem **atributos** (características) e **métodos** (Ações ou comportamentos). Os benefícios de utilizar **POO** são o reciclagem de código, manutenibilidade, escalabilidade, organização e clareza do código e facilidade de colaboração.
# Essencial
---
## Estrutura de uma classe

A estrutura central para a orientação a objetos é a classe. A classe é composta por métodos (funções) e atributos (variáveis), os quais nos aplicar o conceito de abstração. **Abstração** é o ato de descrever um objeto com base nas suas **características** (atributos), **ações** e **comportamentos** (métodos).

```
public class ClasseJava{
	
	#Descrevendo um características de um objeto com variáveis
	
	String atributo1 = valor1;
	int atributo2;
	boolean atributo3 = valor3;
	double atrubuto4;

	#Descrevendo ações e comportamentos de um objeto com métodos
	
	public int acao1(int parâmetro){
		#bloco de código
	}

	public String comportamento1(){
		#bloco de código
	}
}
```

### Instanciação de objetos

```

```

## Pilares do POO

**Abstração**: é o processo de **descrever um objeto** por meio de suas características (atributos), ações e comportamentos (métodos).

**Encapsulamento**: é a prática de **ocultar is detalhes de uma classe** , como atributos e métodos. Podemos controlar quem ou o que pode acessar os detalhes desta classe por meu de métodos definidos dentro da própria classe.

**Herança**: é um mecanismo que permite que uma **classe herde atributos e métodos de outra classe**. É uma relação de pai para filho, uma classe derivada ou subclasse herda os atributos ou métodos de uma superclasse ou classe base.

```

						  +-----------------+
		                  |      Heroi      |
		                  |  (Superclasse)  |
		                  +-----------------+
		                  - nome
		                  - poder
		                  - velocidade()
		                  - forca()
		                  - Voar()
		                  - grudarNaParede()
		                           ^
		                           |
		            +--------------+--------------+
		            |              |              |
			 +-------------+ +-------------+ +-------------+ 
			 |    Flash    | |   Superman  | |  Spiderman  |
			 | (Subclasse) | | (Subclasse) | | (Subclasse) |
			 +-------------+ +-------------+ +-------------+
			 - nome          - nome          - nome
		 	 - poder         - poder         - poder 
			 - velocidade()  - forca()       - forca() 
							 - Voar()        - grudarNaParede()
							 

```

**Polimorfismo**: é a capacidade de **objetos de diferentes classes serem tratados como objetos de uma classe em comum**.

**Sem polimorfismo**, você teria que escrever:

```cachorro.latir()```
```gato.miar()```
```passaro.piar()```

**Com polimorfismo**, poderia cria um método geral ```.fazerSom()``` e associá-los aos objetos:

```cachorro.fazerSom()``` (Ele late)
```gato.fazerSom()``` (Ele mia)
```passaro.fazerSom()``` (Ele pia)

No geral, é a ideia de um mesmo nome ou comando ter muitas formas de comporta-se, dependendo do objeto que o está usando. O polimorfismo está dividido em dois tipos: **polimorfismo estático** e **polimorfismo dinâmico**.

**Polimorfismo estático**: está relacionado a sobrecarga de métodos ou operadores. A sobrecarga é um artifício que permite que vários métodos de uma classe tenham o mesmo nome, mas isso somente é possível se a lista de parâmetros para cada método for diferente. Se houver algum erro ele é resolvido durante o tempo de compilação, por isso o nome estático.

```
int soma(int a, int b);
void soma(float a, double b);
int soma(int a, int b, int c);
```

**Polimorfismo dinâmico**: está relacionado a sobrescrita de métodos. A sobrescrita permite que façamos alteração de métodos em subclasses, ou seja, reescrever uma método que foi herdado da superclasse, dando um outro sentido ou comportamento para ele. Lembrando que os parâmetros e retorno do método tem que permanecer os mesmos da classe pai. Caso ocorra um erro, será identificado durante o tempo de execução.

```
public class Animal{
	public void fazerBarulho(){
		System.out.println("Animal faz barulhos);
	}
}

public class Cachorro extends Animal{

	//sobrescrevendo o método fazerBarulho()
	@override //anotação opcional, porém é uma boa prática.
	public void fazerBarulho(){
		System.out.println("AU AU AU");
	}
}
```
