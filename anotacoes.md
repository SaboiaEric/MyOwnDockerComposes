# Comandos

`docker run`: executar um novo container (rodamos uma imagem), por exemplo `docker run hello-world`.

`docker ps`: lista todos os containers rodando, se adicionar `-a` listamos todos os container mesmo parados.

`docker run -it ubuntu bash`: executa um novo container (com imagem ubuntu), executa o comando bash e o `it` é referente a iteraçao bi-lateral do prompt que abrirá. Para sair do bash usar `crtl + d`

`docker build -t [usuario]/[imagem]:latest`: constroi uma imagem e envia para o usuario/imagem hub.docker.com. Se após `:latest` adicionar ` . ` mencionará qual o docker file será construido

como acessar a porta do container pelo meu computador?

`docker run -p 8080:80 nginx`: roda um container (com imagem nginx) e ao publicar faz com que a portal 8080 da máquina publicada acesse a porta 80 do container.

`docker exec {nome_container} ls`: executa um comando ls no container {nome_container}

`docker run -p 8080:80 -v $(pwd)/html:/usr/share/nginx/html nginx`: cria executa e cria um container em uma pasta compartilhada entre o container e o computador local.

`docker-compose.yaml`: é um manifesto para descrever quais imagen eu quero rodar.

Exemplo de execução do banco de dados localmente: 

`docker run -e 'ACCEPT_EULA=Y' -e 'SA_PASSWORD=Pass@word' -p 5433:1433 -d mcr.microsoft.com/mssql/server:2019-latest`