# despr2_1_apache
Instalación y despliegue básico con Apache

## Tareas Paso a Paso 
Creacion de la VM

![alt text](/images/image.png)

Configura la red

![alt text](/images/image-1.png)

Inicia la VM por SSH desde el Host

![alt text](/images/image-2.png)

## Preparación del entorno
Actualiza los Paquetes
![alt text](/images/image-6.png)


Instala apache2

![alt text](/images/image-5.png)

Configura el firewall para permitir tráfico HTTP y HTTPS:
Verifica que las reglas se han aplicado:
Si no está configurado, habilita el tráfico ssh, HTTP y HTTPS
Habilita el firewall si no está habilitado

![alt text](/images/image-7.png)

### Comprobación básica
Comprueba que el servicio está activo

![alt text](/images/image-9.png)

Desde el host, accede a http://localhost:8081/ y comprueba que ves la página por defecto de Apache

![alt text](/images/image-10.png)

### Desplegar el sitio de ejemplo
Copia los archivos del sitio de ejemplo a /var/www/html/
Utiliza scp desde tu máquina local:
![alt text](/images/image-11.png)

En la VM crear la estructura de carpetas
Ajustar los permisos y propiedad de los archivos para que Apache
pueda servirlos correctamente:
:
![alt text](/images/image-12.png)


### Comprobar
![alt text](/images/image-13.png)


### Problemas encontrados:

Tuve algunos problemas para configurar los puertos de la máquina, lo que impedía acceder por SSH y HTTP desde el host. Eliminé las reglas de NAT antiguas y creé nuevas reglas correctamente para SSH (2223 → 22) y HTTP (8081 → 80), lo que me permitió conectarme y desplegar el sitio sin problemas.