#Apache vs Nginx: ¿qué servidor web debo montar este 2019?


##Nginx vs Apache: quién es más rápido y quién consume menos recursos

 la verdad es que los dos son servidores muy rápidos, sobre todo en webs y plataformas con pocos usuarios simultáneos. Sin embargo, cuando el número de usuarios aumenta sí que notamos que a Apache le empieza a costar trabajar con tantos usuarios al mismo tiempo, mientras que Nginx se comporta mucho más rápido cuando tenemos mucho tráfico.

##Apache vs Nginx: quién es más fácil de configurar
Apache es, de lejos, mucho más sencillo de configurar y poner en marcha. Apache, además, es un servidor web infinitamente más flexible que Nginx gracias a las .htaccess tools y a los más de 60 módulos diferentes que podemos encontrar.

aunque Apache puede ganar en facilidad y flexibilidad, no podemos cerrar este apartado sin mencionar uno de los puntos fuertes de Nginx, y es que este servidor es mucho más intuitivo al trabajar con varios hostings, estando todos ellos separados y en directorios independientes.

##Nginx vs Apache: quién es más seguro
Otro aspecto fundamental de un servidor web es la seguridad. En esta ocasión, ambos servidores empatan,

##Entonces, ¿cuál es mejor? Apache vs Nginx

 Mientras que si vamos a montar una página web muy grande que contará con muchos usuarios diarios la mejor opción es usar Nginx por sus mejoras de rendimiento, si queremos algo sencillo y flexible, Apache será un servidor mucho más apropiado, sobre todo para los usuarios sin muchos conocimientos.

 ##


 First, create the /data/www directory and put an index.html f
https://www.digitalocean.com/community/tutorials/como-instalar-nginx-en-ubuntu-18-04-es
 sudo apt install nginx

 Configurar el Firewall

 sudo ufw app list

 Como puede ver, hay tres perfiles disponibles para Nginx:

Nginx Full: Este perfil abre tanto el puerto 80 (tráfico web normal, no cifrado) como el puerto 443 (tráfico TLS/SSL cifrado)
Nginx HTTP: Este perfil solamente abre el puerto 80 (tráfico web normal, no cifrado)
Nginx HTTPS: Este perfil solamente abre el puerto 443 (tráfico TLS/SSL cifrado)
Debido a que en esta guía todavía no configuramos SSL para nuestro servidor, únicamente vamos a tener que permitir tráfico en el puerto 80.

Puede habilitar esto ingresando:

sudo ufw allow 'Nginx HTTP'

Puede verificar el cambio ingresando:

sudo ufw status
Status: active
----
https://www.digitalocean.com/community/questions/sudo-ufw-status-return-inactive
Status: inactive ??
sudo ufw enable
sudo ufw default deny
----


Paso 3 — Verificar su servidor web
systemctl status nginx /// run active
http://165.22.203.55/


saber nuestra IP 
ip addr show eth0 | grep inet | awk '{ print $2; }' | sed 's/\/.*$//'

Paso 4 — Gestionar el proceso de Nginx

sudo systemctl stop nginx

sudo systemctl start nginx

sudo systemctl restart nginx

sudo systemctl reload nginx // sin perder conecciones 


//configuracion prdeterminada para que inicie ngnix poc el servidor
sudo systemctl disable nginx

sudo systemctl enable nginx
