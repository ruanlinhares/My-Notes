**(Notas atualizadas em 14/07/2025)**

# Iniciando
---
**IDEs recomendadas:** Intellij, Eclipse.

**JDK:** Java Development Kit (Pacote para desenvolvedores).

**JRE:** Java Runtime Enviroment (Pacote para usuários comuns que desejam executar uma aplicação java).

Para deixar claro, precisamos baixar o pacote de desenvolvimento do java (**JDK**) e alguma IDE ou editor de código.

## Processo de compilação

Atualmente é comum que diversas linguagens de programação sejam chamadas de linguagem de **alto nível**, pois sua comunicação é mais próxima da linguagem humana. Com o Java acontece o mesmo: ele é uma linguagem de alto nível que, assim como outras, precisa ser compilada para ser executada em máquinas. Nesse processo existia um problema, cada código-fonte é escrito somente para um sistema operacional ou modelo de processador,o que implicava na necessidade de escrever vários códigos para máquinas diferentes. O Java vem para quebrar isso. Ele permite que um código-fonte possa ser executado em qualquer máquina, e isso acontece através da **JVM** (Java Virtual Machine).

```
Código java (.java) --> Compilador (Javac) --> Bytecode(.class) --> JVM (Java Virtual Machine) --> CPU (execução na máquina destino)
```

Neste exemplo, o código-fonte é enviado para o compilador, o compilador, então transforma esse código em para linguagem de máquina (bytecode). Por fim, esse **bytecode** é interpretado pela JVM (Java Virtual Machine). A JVM precisa estar intalada no lado do cliente, seja por meio do **JDK** (Java Development Kit) ou do **JRE**(Java Runtime Enviroment).
# Essencial
---
## Variáveis

Java é uma linguagem estaticamente tipada, isso significa que o programador deve definir o tipo de dado para uso em variáveis e funções. Diferente de outras linguagens como Python e javascript que são dinâmicamente tipadas. Nessas, não é necessário definir os tipos de dado. 

Exemplo de alguns tipos essenciais em java:

```
# Classe para valores de textos
String nome = "Mark Grayson";

#tipo para valores inteiros e decimais
int idade = 17;
double forca = 57.03;
float velocidade = 35.00f; # valores float devem ser acompanhados por "f" ou "F"  

#tipos para valores booleanos
boolean viltrumita = true;
```

Algumas observações devem ser feitas. Primeiramente, as classes, variáveis e métodos em java devem ser definidas no padrão **camelCase** (para variáveis e métodos) ou **PascalCase** (para classes). As variáveis e métodos devem possuir a primeira letra no minúsculo. Utiliza-se letras maiúsculas, no início, somente em classes, para melhor identificação de cada coisa. Pois, podemos ter uma variável ou método com o mesmo nome da classe. 

Além disso, outra observação que devemos fazer é sobre os valores float. Eles devem ser escritos com a letra "f" ou "F" no final, pois, em java, os valores com ponto flutuante são definidos por padrão como tipo ```double```. Portanto, não podemos inserir um valor double me uma variável do tipo float, ocorre erro de compilação.