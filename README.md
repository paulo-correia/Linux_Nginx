# Nginx

![](https://github.com/paulo-correia/Linux_Nginx/blob/master/Nginx_logo.png)

Nginx \[engine x\] é um servidor proxy HTTP e reverso, bem como um servidor de proxy de email, escrito por Igor Sysoev desde 2005.

O Nginx é um servidor web rápido, leve, e com inúmeras possibilidades de configuração para melhor performance

## Instalação

Toda a instalação é feita como root

### Debian

Instale o pacote do nginx com o comando:

 `apt-get install nginx`

Teste abrindo o IP do servidor/máquina num navegador

### CentOS

 Instale o repositório EPEL com o comando:

 ` yum -y install epel-release`

Inicie o serviço com o comando:

 ` systemctl start nginx`

Coloque o serviço para ser carregado no boot com o comando:

 ` systemctl enable nginx`
