**(Notas atualizadas em 06/08/2025)**

# Iniciando
---
**Programação orientada a objeto (POO)** é um paradigma usado por algumas linguagens como o java, C++, Python. Ela surge para encapsular, e assim, organizar código em torno de objetos em vez de funções ou lógica. **POO** visa modelar o mundo real  dentro do código, representando entidades como objetos que possuem **atributos** (características) e **métodos** (Ações ou comportamentos). Os benefícios de utilizar **POO** são o reciclagem de código, manutenibilidade, escalabilidade, organização e clareza do código e facilidade de colaboração.
# Essencial
---
## Estrutura de uma classe

A estrutura central para a orientação a objetos é a classe. A classe é composta por métodos (funções) e atributos (variáveis), os quais nos aplicar o conceito de abstração. **Abstração** é o ato de descrever um objeto com base nas suas **características** (atributos), **ações** e **comportamentos** (métodos).

```JSX
public class ClasseJava{
	
	//Descrevendo um características de um objeto com variáveis
	
	String atributo1 = valor1;
	int atributo2;
	boolean atributo3 = valor3;
	double atrubuto4;

	//Descrevendo ações e comportamentos de um objeto com métodos
	
	public int acao1(int parâmetro){
		//bloco de código
	}

	public String comportamento1(){
		//bloco de código
	}
}
```

### Instanciação de objetos

Após a criação das classes, é necessário fazer a instanciação de um objeto para dentro de uma variável do mesmo tipo da classe criada. Observe:

```JSX
public class Animal{
	//bloco de código;
}

//fazendo a instanciação na main

Animal animal1 = new Animal();
```

Perceba que acima criamos uma variável chamada ```animal1``` do tipo por referência ```Animal```. Dentro dela faremos um ponteiro para um novo objeto do tipo ```Animal```. Chamamos, agora, as classes criadas de tipos por referência, pois a variável não armazena o objeto em si, mas sim uma referência (endereço na memória) para onde o objeto ```Animal``` está armazenado.
## Pilares do POO

### Abstração

É o processo de **descrever um objeto** por meio de suas características (atributos), ações e comportamentos (métodos).

### Encapsulamento

É a prática de **ocultar is detalhes de uma classe** , como atributos e métodos. Podemos controlar quem ou o que pode acessar os detalhes desta classe por meu de métodos definidos dentro da própria classe. Para isso, necessitamos de artifícios chamados de **Controladores de acesso**, eles dividem-se em 3 mais usados:

**Public**: com esse modificador, o acesso aos membros de uma classe(atributos e métodos) é **totalmente liberado**. Eles podem ser acessados de qualquer lugar do programa: pela **própria classe**, por **suas subclasses** ou por **classes externas**.

**Protect**: Este modificador restringe o acesso, permitindo que os membros sejam acessados apenas pela **própria classe** e por suas **classes filhas** (subclasses). O acesso é negado para classes externas que não façam parte da hierarquia de herança.

**Private**: esse modificador é o mais restritivo. Proíbe o acesso a **qualquer** **membro fora da própria classe**. Classes filhas (subclasses) e classes externas não podem acessar os membros intitulados como private. 

| MODIFICADOR/ACESSO | Própria classe | Classes filhas | Classes externas |
| ------------------ | -------------- | -------------- | ---------------- |
| **Public**         | sim            | sim            | sim              |
| **Protect**        | sim            | sim            | não              |
| **Private**        | sim            | não            | não              |

**Setters**

Em programação, um setter é um método que modifica um valor, seu objetivo em **POO** é modificar o valor das propriedades de um objeto. Ele é parte fundamental do conceito de **encapsulamento.** Geralmente, tem a nomenclatura do método escrita dessa maneira: setalgumAtributo(). O setter recebe um parametro que será o novo valor da variável de instância. Estrutura de um setter:

```jsx
private String poder;

public void setpoder(String poder){
	this.poder = poder;
}
```

O termo **this** é opcional, é usado para diferenciar a **variável do objeto atual** de um **parâmetro de método com mesmo nome**. O compilador fica consfuso sobre quem está atribuindo valor a quem. Mas poderiamos reescrever assim:

```jsx
// Certo!!!!
//-----------

private String poder;

public void setpoder(String novoPoder){
	poder = novoPoder;
}

// Erro de compilação
//---------------------
private String poder;

public void setpoder(String poder){
	poder = poder;
}
```

Podemos fazer blocos de código dentro do setter que permita ou negue essa atribuição de valor. Utilizando condicionais, repetições (loops) e métodos, podemos fazer regras para permitir e negar essa alteração de atributos.

### Herança

É um mecanismo que permite que uma **classe herde atributos e métodos de outra classe**. É uma relação de pai para filho, uma classe derivada ou subclasse herda os atributos ou métodos de uma superclasse ou classe base.

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

Podemos fazer essa herança a partir do de um termo chamado ```extends```, ele é usado na declaração de uma classe para informar de qual superclasse ele estará herdando. Uma classe somente pode herdar de uma outra única classe, uma relação de 1 para 1. Exemplo:

```JSX
//Superclasse exemplo
public class Animal{
	String atributo1;
	int atributo2;

	public void metodo1(){}
	pulbic int metodo2(){}
}

//subclasse exemplo

public class Cachorro extends Animal{
	String atributo1;
	
	public void metodo1(){}
	pulbic int metodo2(){}
}

```
### Polimorfismo

É a capacidade de **objetos de diferentes classes serem tratados como objetos de uma classe em comum**.

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

```jsx
int soma(int a, int b);
void soma(float a, double b);
int soma(int a, int b, int c);
```

**Polimorfismo dinâmico**: está relacionado a sobrescrita de métodos. A sobrescrita permite que façamos alteração de métodos em subclasses, ou seja, reescrever uma método que foi herdado da superclasse, dando um outro sentido ou comportamento para ele. Lembrando que os parâmetros e retorno do método tem que permanecer os mesmos da classe pai. Caso ocorra um erro, será identificado durante o tempo de execução.

```JSX
public class Animal{
	public void fazerBarulho(){
		System.out.println("Animal faz barulhos);
	}
}

public class Cachorro extends Animal{

	//sobrescrevendo o método fazerBarulho()
	@Override //anotação opcional, porém é uma boa prática.
	public void fazerBarulho(){
		System.out.println("AU AU AU");
	}
}
```


## Interfaces