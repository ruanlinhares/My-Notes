**(Notas atualizadas em 10/07/2025)**
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

Estrutura básica de um arquivo ```.vue```:

```
<template>
	Seu código HTML
</template>

<script>
	Seu código JS ou TS
</script>

<style>
	Seu código CSS
</style>
```

## Importação de componentes

No **Vue** trabalhamos diretamente com a importação de componentes. Botões são componentes, seções (main, header, footer) são componentes e páginas são compontenes.

Na tag ```<script>``` de cada arquivo ```.vue``` poderemos fazer a chamada de outros componentes:

```
<script>
#importa o modulo (componente) desejado
import nome-do-componente from ./path/do/componente

# Dá nome ao componente atual e registra usos de outros componentes
export default {
	name: 'componente-atual',
	components:{
		componente-1,
		componente-2,
		componente-3
	}
}
</script>
```

De uma forma mais detalhada, o ```export default{}``` funciona como a planta baixa de uma casa, a casa é nosso componente. Ele é usado para dar nome ao componente, assim ele pode ser identificado facilmente e permite que ele faça recursividade, além de registrar quais componentes ele carrega em si e que usará na tag ```<template>```. Existem outras funções e atributos para o objeto de configuração. Aqui usamos as propriedades name e components, mas existem data, methods, props, computed e watch.

## Diretivas v-if/v-show/v-for/v-bind

Diretivas são instruções que o **Vue** atribui aos elementos HTML. As diretivas são muito usadas. No HTML puro temos diretivas como ```alt```, ```src```, ```placeholder``` e outros. O vue adiciona diretivas especiais ao elemento HTLM . 

### Condicionais v-if e v-show

Podemos usar diretivas de condicional par mudar o estado de um elemento html ou ocultá-lo.

```
import ImageLogo from ./components/ImageLogo.vue
import AdminTab from ./components/AdminTab.vue
import DeveloperTab from ./components/DeveloperTab.vue
import UserTab from ./components/UserTab.vue

<template>
	<ImageLogo
		v-show="showImageLogo" # Ocultar ou exibir o elemento
	/>
	<AdminTab
		v-if="accessLevel == 'admin'"
	/>
	<DeveloperTab
		v-else-if="accessLevel == 'developer'"
	/>
	<UserTab
		V-else
	/>
</template>

<script>
export default{
	name: 'component-name',
	components:{
		ImageLogo,
		AdminTab,
		DeveloperTab,
		UserTab
	},
	data(){
		return{
		 showImageLogo: false, #objeto reativo
		 accessLevel: 'admin'
		}
	}
}
</script>
```

Agora, estamos trabalhando com uma função chamada ```data()``` no ```export default{}```. Essa função retorna um objeto e tudo que estiver dentro dele é chamado de objeto reativo. Ele pode receber um valor bool, string, número, vetore(arrays) até mesmo outro objeto. É através dessas propriedades reativas que ```data()``` retorna que gerenciamos o estado do componente.

**v-if VS v-show - Qual a diferença?**

**v-if** : Esconde ou mostra o elemento removendo ou adicionando no DOM. Ele literalmente cria ou destrói o elemento.

**v-show** : Esconde ou mostra o elemento desabilitando-o visualmente. Ele permanece no DOM, porém seu style ganha a propriedade ```display: none``` para ocultar, e para mostrar, essa propriedade é removida. 

**OBS**: o comando ```v-if``` vai consumir mais processamento, então ficar atento para a interface não ficar pesada e lenta.

### Loops V-for





