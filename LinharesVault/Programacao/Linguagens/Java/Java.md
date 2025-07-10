**(Notas atualizadas em 10/07/2025)**

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
