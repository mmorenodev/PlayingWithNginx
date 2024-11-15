# PlayingWithNginx

### Directivas
Función que realiza una acción, las directivas están compuestas de un nombre, seguida de un conjunto de parámetros.
La principal característica de una directiva es que esta debe encontrarse dentro de un contexto; tomar en cuenta que algunas directivas solo pueden funcionar dentro de un contexto en específico. 

### Contextos
Un contexto es una directiva en la que definimos un cuerpo, el cual puede contener múltiples directivas 
<img width="350" alt="image" src="https://github.com/user-attachments/assets/705ae2e9-59cd-48b8-8052-058e881bc539">

### Core Contexts
La siguiente lista de contextos nos permiten básicamente definir la funcionalidad de nuestro servidor Nginx 
1. Main
2. Events: utilizado para definir la configuración sobre las conexiones de usuario. Por ejemplo, la cantidad de conexiones a aceptar, número de procesadores, etc. Este contexto se puede definir una sola vez dentro de Nginx. Podemos llegar a ver este tipo de contextos (los que se definen una sola vez) como globales, ya que afectan en general el funcionamiento de Nginx.
3. Http: en este contexto definimos las directivas para la administración de las peticiones Http, así como Https. 
4. Server: este es un contexto que definimos dentro del contexto Http para poder trabajar con múltiples configuraciones. Aquí utilizaremos directivas para configurar nuestro host, por ejemplo el puerto a escuchar, los archivos a retornar, etc. 
5. Location: a través de este podemos cambiar el comportamiento de una petición, por ejemplo redirigir al usuario cada vez que acceda a la ruta /admin.
6. Upstream: definimos a un conjunto de servidores para balanceo de cargas, proxy reversivo. 
7. Mail
8. If


Nginx trabaja a través de una estructura de árbol la cual contiene a un conjunto de contextos, dentro de toda la configuración de Nginx el primer contexto que contiene a toda la configuración es llamado 'Main'.
Main es el único contexto que no contiene un cuerpo.




