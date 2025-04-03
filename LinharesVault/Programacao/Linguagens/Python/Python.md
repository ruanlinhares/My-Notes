# Python - Variáveis e tipos

"A linguagem Python possui diferentes tipos(objetos) de dados, mas no final os tipos em são objetos".

Alguns tipos de dados que são mais trabalhados:
<table>
    <tr>
        <th>Tipos</th>
        <th>Exemplos</th>
    </tr>
    <tr>
        <th>int</th>
        <th>10 | -4 | 100</th>
    </tr>
    <tr>
        <th>float</th>
        <th>10.5 | -0.223 | 3.58</th>
    </tr>
    <tr>
        <th>String</th>
        <th>"Hello World"</th>
    </tr>
    <tr>
        <th>Boolean</th>
        <th>0 or 1 || True or False</th>
    </tr>
</table>


### Variáveis

São espaços nomeados da memória que armazenam algum valor dos tipos acima, podemos ter dois tipos de atribuição, única ou múltiplas.

```
#Exemplo de atribuição de variáveis SIMPLES

nome = "Harry Potter"

idade = 16

altura = 1.79

trouxa = False

#Exemplo de atribuição de variáveis MÚLTIPLAS

nome, idade, altura, trouxa = "Harry Potter", 16, 1.79, False   
```
Em Python diferente de outras linguagens como Java ou C, não é necessário delaclarar 
o tipo do dado antes da variável, pois de ela não é compilada, o interpretador python faz o 
reconhecimento automaticamente. Outro detalhe é que em Python "não existe" o tipo char todo 
tipo de caracter é definido com string e não se faz necessario utilizar apóstrofo ou 
aspas para diferenciar os tipos char e string, podemos utilizar as duas sinalizações para 
indicar uma string uma string.

### Função type()

Usamos a função **type()** para descobrir o tipo de uma variável. Exemplo:

```
type(nome)

out: str
----------------

type(idade)

out: int
----------------

type(altura)

out: float
----------------
```
### Função dir()

A função dir() descobre metodos associados a um tipo(objeto):

```
dir(nome)

out: ['upper',
      'lower',
      'split'
      'swapcase']

#Existem muito mais funções associadas ao objeto string, mas por convenção citei somente
alguma. 
```