# WordPress Stack com Docker Swarm - MariaDB

Este repositório contém os arquivos necessários para implantar uma stack WordPress utilizando o Docker Swarm. A configuração inclui o WordPress, o banco de dados MariaDB e suporte para volumes persistentes.

1. Estrutura do Projeto

- Docker Swarm
- NFS Server
- MariaDB
- Wordpress
- Git

2. Implemente a stack

Use o comando abaixo para iniciar os serviços no Swarm:

docker stack deploy -c wordpress.yml -d wordpress

3. Acesse o WordPress

Após o deploy, abra o navegador e acesse:

WordPress: http://localhost:8080 (ou os ips dos nós do swarm)

4. Configuração do Docker Compose

Serviços
WordPress:

Utiliza a imagem oficial do WordPress.
Configurado para se conectar ao banco MariaDB na mesma rede.
Dados persistem no volume wp_data.

MariaDB:

Utiliza a imagem oficial do MariaDB.
Armazena os dados no volume db_data.

Volumes
wp_data: Armazena os arquivos do WordPress (temas, plugins, uploads).
db_data: Armazena os dados do banco de dados MariaDB.

5. Contribuindo

Contribuições são bem-vindas! Sinta-se à vontade para abrir uma issue ou enviar um pull request.

