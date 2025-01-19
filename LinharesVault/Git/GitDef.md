# Git : Controle e versionamento de código
O Git é utilizado para fazer o gerenciamento das versões de um código fonte  mais facilmente sem ter o risco de perder o controle dessas versões.

## Sistemas de controle de versão
Os sistemas de controle de versão controlam o arquivo ao longo do tempo, eles possuem algumas responsabilidades como:

* Registrar o histórico  de atualizações de arquivos.
* Gerenciar quais foram as alterações, a data de alteração, quem alterou, etc.
* Organização, controle e segurança.
  
### Tipos de sistemas de controle de versão

* <b>VCS Centralizado (CVCS) :</b> Nesse tipo de sistema de vesionamento temos apenas um servidor que irá conter todos os arquivos responsáveis pelo controle de versão, e somente podemos trabalhar no código com o servidor no ar, ou seja, caso o servidor fique fora do ar em algum momento perdemos a possibilidade de trabalhar no projeto. 

* <b>VCS Distribuído (DVCS) :</b> Nesse tipo de sistema de versionamento além de existir um servidor com o controle das versões, esse mesmo servidor é clonado em uma máquina localmente, permitindo a edição no código fonte mesmo que o servidor esteja fora do ar, pois estaremos com os arquivos da vesão baixados em nossa máquina locamente, posteriormente podendo enviar nosso trabalho para o servidor central sem perder produtividade.

## Git != Github

* <b>Git :</b> O git como citado anteriormente é um sistema de controle de versionamento ele atua somente na parte de controle e segurança para o código mais ainda precisamos de um servidor para alocar essas versões do código certo?

* <b>Github, GitLab, BitBucket, CodeBerg :</b> Sistemas como o github, são resposáveis por hospedar as nossas versões de código, muito utilizado pela comunidade para salvar versões do código dos seu projetos, eles atuam literalmente como um servidor particular para cada usuário, cada user tem a possibilidade de subir seus projetos em um lugar seguro e trabalhar de maneira individual ou compartilhada com diversos outros users, incusive essa anotação está hospedada Github e CodeBerg neste exato momento.