# despr2_1_apache
Instalación y despliegue básico con Apache

## Tareas Paso a Paso 
Creacion de la VM

![alt text](image.png)

Configura la red

![alt text](image-1.png)

Inicia la VM por SSH desde el Host

![alt text](image-2.png)

## Preparación del entorno
Actualiza los Paquetes
![alt text](image-6.png)


Instala apache2

![alt text](image-5.png)

Configura el firewall para permitir tráfico HTTP y HTTPS:
Verifica que las reglas se han aplicado:
Si no está configurado, habilita el tráfico ssh, HTTP y HTTPS
Habilita el firewall si no está habilitado

![alt text](image-7.png)

### Comprobación básica
Comprueba que el servicio está activo

![alt text](image-9.png)

Desde el host, accede a http://localhost:8081/ y comprueba que ves la página por defecto de Apache

![alt text](image-10.png)

### Desplegar el sitio de ejemplo
Copia los archivos del sitio de ejemplo a /var/www/html/
Utiliza scp desde tu máquina local:
![alt text](image-11.png)

En la VM crear la estructura de carpetas
Ajustar los permisos y propiedad de los archivos para que Apache
pueda servirlos correctamente:
:
![alt text](image-12.png)


### Comprobar
![alt text](image-13.png)