# Configuração de rotas (PHP)

Para iniciar uma configuração de rotas depende do seu nível de necessidade e se estiver utilizando algum framework. Aqui apresentam-se algumas abordagens mais comuns:
### 1. Sem Framework (Routing "Manual")

Essa abordagem se baseia na manipulação da variável superglobal ```$_SERVER[]``` para determinar qual conteúdo exibir ou qual ação executar.

```
<?php 

//Captura a URL requisitada pelo navegador
$uri = $_SERVER['REQUEST_URI']; 

//Compara a URL para redirecionar para o conteúdo ou ação
switch ($uri) { 
	case '/': 
		require 'home.php'; 
		break; 
	case '/sobre': 
		require 'sobre.php'; 
		break; 
	case '/contato': 
		require 'contato.php'; 
		break; 
	case '/produto/123': 
		// Lógica para exibir o produto com ID 123 
		echo "Exibindo o produto 123"; 
		break; 
	default: 
		http_response_code(404); 
		require '404.php'; 
		break; 
} 

?>
```

- Esse código estará encapsulado em um arquivo PHP (Geralmente chamado ```index.php```). Visto isso, será necessário configurar um servidor web (Apache, Nginx, etc.) para redirecionar todas as requisições para esse arquivo PHP. Isso é feito através de regras de reescrita de URL (mod_rewrite no Apache, por exemplo).

- Você terá que lidar com métodos HTTP e parâmetros da URL. Essa abordagem pode se tornar complexa para projetos maiores com muitas rotas.

! escrever sobre url amigavel usando o mod_rewrite do apache
### 2. Utilizando um Micro-Framework de Routing

### 3. Utilizando um Framework PHP Completo





