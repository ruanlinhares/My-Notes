**(Notas atualizadas em 10/07/2025)**
# Iniciando

---

O trabalho da programação em Assembly é manipular dados na memória principal e nos registradores com as instruções da CPU. Aqui vamos ter uma mistura entre linguagens de baixo e alto nível. Precisaremos de ferramentas mistas.

## Ferramentas

**Editor de texto (Recomendações):** Vim, Visual Studio Code, Nano, sublime ou bloco de notas. Escolha livre.

**Montador:** NASM (Netwide Assembler), um montador para arquiteturas x86-16 bits, x86-64 bits e IA-32 bits.

**Ligador:** GNU id, é a ferramenta que transforma os pedaços compilados do código (**Arquivos objeto/código objeto**) em um programa funcional. O **código objeto -** código gerado pelo compilador, é uma versão binária das instruções do seu código fonte. Específica para a arquitetura do processador do seu computador. Ele ainda não é um programa pronto para ser executável.

**Compilador:** Gnu gcc (Linguagem C), GNU g++ (linguagem C++).

**Makefiles:** GNU make, é uma ferramenta para automatizar o processo de compilação, sem a necessidade de passar o comando ao shell. Será criado um arquivo, geralmente chamado **makefile**. Ele é escrito para instruir como será construído o projeto, utilizando uma série de regras para isso.

**Depurador:** GNU debugger (GDB), é uma ferramenta que permite executar o código de forma controlada, permite que você observe passo a passo como o código está rodando verificando seu status.

**Editor Hexadecimal:** Hexeditor, é um programa que permite visualizar e editar conteúdo binário de qualquer arquivo diretamente a nível de bytes.

**Hex Dumper:** xxd, é uma ferramenta que lê o conteúdo de um arquivo e exibe, em linhas, os valores em hexadecimal, byte a byte. Também pode fazer a conversão de arquivos hexadecimal em binário e vice-versa.

**Editor Hexadecimal VS Hex Dumper?**

**Editor Hexadecimal:** Permite a visualização e edição direta de um arquivo hexadecimal, você pode abrir o arquivo e clicar em qualquer byte que deseja editar.

**Hex Dumper:** Permite a visualização e conversão dos arquivos em hexadecimal. Caso queira editar é necessário salvar o dump do binário em um arquivo .txt, alterá-lo e depois converter para binário novamente. **Nota:** o processo é mais complexo com para editar no xxd.