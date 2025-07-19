**(Notas atualizadas em 17/07/2025)**

# Iniciando
---
**Programação orientada a objeto (POO)** é um paradigma usado por algumas linguagens como o java. Ela surge para encapsular, e assim, organizar código em torno de objetos em vez de funções ou lógica. **POO** visa modelar o mundo real  dentro do código, representando entidades como objetos que possuem **atributos** (características) e **métodos** (Ações ou comportamentos). Os benefícios de utilizar **POO** são o reciclagem de código, manutenibilidade, escalabilidade, organização e clareza do código e facilidade de colaboração.

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
			 - velocidade()  - força()       - forca() 
							 - Voar()        - grudarNaParede()

```

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
public class Main {

	public static void main(String[] args){
		
		
	}
}
```


