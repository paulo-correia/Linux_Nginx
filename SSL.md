## SSL
Habilita o certificado de sites, SSL na porta **443**

## Instalação
Toda a instalação é feita como **root**

Crie a pasta ssl dentro de /etc/nginx usando o comando:

mkdir /etc/nginx/ssl

### Exemplo de configuração
Arquivo /etc/nginx/conf.d/example_ssl.conf:

```
# HTTPS server
#
server {
   listen       443 ssl;
   server_name  localhost;

   ssl_certificate      /etc/nginx/ssl/nginx.crt;
   ssl_certificate_key  /etc/nginx/ssl/nginx.key;

   ssl_session_cache shared:SSL:10m;
   ssl_session_timeout  5m;

   ssl_ciphers  "EECDH+ECDSA+AESGCM EECDH+aRSA+AESGCM EECDH+ECDSA+SHA384 EECDH+ECDSA+SHA256 EECDH+aRSA+SHA384 EECDH+aRSA+SHA256 EECDH+aRSA+RC4 EECDH EDH+aRSA RC4 !EXPORT !aNULL !eNULL !LOW !3DES !MD5 !EXP !PSK !SRP !DSS";
   ssl_prefer_server_ciphers   on;

   ssl_protocols TLSv1 TLSv1.1 TLSv1.2;

   location / {
       root   /usr/share/nginx/html;
       index  index.html index.htm;
   }
}
```

Reinicie o serviço do nginx com o comando:

`service nginx restart`

## Testes

Teste abrindo o IP do servidor/máquina num navegador colocando https:// na frente
