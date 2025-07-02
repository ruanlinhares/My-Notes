**(Notas atualizadas em 01/07/2025)**
# Iniciando
---

Utilize o comando abaixo para adicionar o Vue ao gerenciador de pacotes:

```
npm install vue
```

Após criar o diretório ou clonar um repositório escreva esse comando no seu shell para criar um app vue, podemos usar o vue/cli ou vite:

```
npm create vue@latest # cria o app via vue/cli

npm create vite@latest # cria o app via vite
```

Assim que o app for criado é necessário passar o seguinte comando ao shell, faça isso dentro da pasta do projeto vue:

```
npm install
```

O motivo é fazer com que todas as dependências do **package.json** que o projeto possui sejam instaladas no diretório node_modules deste projeto em específico. Assim, tudo funciona normalmente. O node global não sofre alterações.

# Essencial
---
O vue é um framework baseado na montagem de componentes visuais. Ele utiliza um conceito de SFC (Single File Component), isso significa que o componente é escrito em um arquivo. Seu HTML, CSS e Typescript ou Javascript estão contidos em um arquivo único. Esse conceito facilita, já que alguns framewoks como o Angular separam a estrutura, estilo e código em no mínimo 3 arquivos.