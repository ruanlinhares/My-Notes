**(Notas atualizada em 07/09/2025)**
# Iniciando
---
O NestJs é um framework para desenvolvimento back-end que utiliza as linguagens JavaScript, TypeScript e o interpretador NodeJs. Construído em TypeScript, é robusto para a criação aplicações **server-side**, garantindo escalabilidade e manutenabilidade a longo prazo. Por baixo dos panos, o framework se alimenta de outros **frameworks HTTP server**, como Express ou Fastfy.

Instalação do framework no gerenciador de pacotes **NPM**:

```bash
npm install -g @nestjs/cli
```

Criando um novo projeto:

```bash
nest new nome-do-projeto
```

Para uma instalação mais completa podemos adicionar o **Typeorm(ORM)** e o **Typerorm para Nestjs** (ele adiciona mais funcionalidades ao typeorm que são exclusivas para NestJs) no diretório do novo projeto:

```bash
npm install @nestjs/typeorm typeorm
```

# Essencial
---
O NestJs utiliza uma arquitetura de separação de responsabilidades, baseada em frameworks como que divide seus códigos em 3 partes. Essas partes são: **Controllers**, **Services** e **Modules**.

### Controllers

```ts
import { Body, Controller, Get, Post } from "@nestjs/common";
import { Projeto } from "src/Projetos/projeto.model";
import { ProjetoService } from "src/Projetos/projeto.service";

@Controller("/projetos")
export class ProjetoController {
	// injetando dependecia do service
	constructor(private readonly projetoService: ProjetoService){}

	@Post()
	inserirProjeto(@Body() novoProjeto: {nome:string; descricao:string; criadorProjeto:string}): Promise<Projeto> {
		return this.projetoService.inserir(novoProjeto);
	}
	
	@Get()
	listarProjetos(): string{
		return "oi, aqui estão os projetosss!!";
	}
}
```

O código acima exibe a estrutura de um controller em TypeScript no NestJs. É uma classe com formato semelhante a java, php ou c++, porém está presente, aqui, o conceito de **Decorators**. Fornecido pelo NestJs, essa funcionalidade permite-nos marcar a classe como um **@Controller** e definir uma rota padrão, além de marcação de requisições padrao **@Get**, **@Post** e **@Body**, essa última é utilizada para capturar corpo das requisições.

### Services

```ts

```