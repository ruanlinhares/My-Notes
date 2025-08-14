(Notas atualizadas em 01/07/2025)
# Iniciando
---
#### Instalar o Angular

```
npm install -g @angular/cli
```

#### Criar novo projeto

Podemos fazer a criação do projeto diretamente pelo angular.

```
ng new <project-name>
```

Ou podemos utilizar o **Vite** (minha preferência atualmente).

```
npm create vite@latest
```

#### Extensões interessantes (VSCode)

- Angular Snippets

**Snippets** são blocos de código que agilizam o desenvolvimento, eles podem ser criados ou utilizados de alguma extensão.

# Visão geral do projeto
---

![[Screenshot from 2025-01-27 06-50-38.png]]

O projeto angular em uma visão rápida é dividido entre o meu **index.html** que chama o arquivo **app.component.html**, dentro do mesmo podemos importar nossos componentes que serão exibidos.

# Components
---
No angular cada componente criado É composto por 3 arquivos principais:

![[Screenshot from 2025-01-27 07-16-09.png]]

Um Aquivo **HTML**, um aquivo **CSS** ou **SCSS** e um arquivo **JavaScript** ou **TypeScript**. O esquema funciona assim como no HTML, CSS e js puro, a diferença é que esses componentes podem ser reciclados e utilizados durante todo o projeto facilmente. Uma boa prática é criar uma pasta **pages** para seus componentes tipo página, é dentro desses componentes que iremos importar nossos componentes da pasta **components**.

# Bootstrap

# Funções

## NgOnInit 
## NgDestroy

## NgIf

## NgDoCheck

