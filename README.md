## Paso 1: Preparar y Configurar Portainer
Ahora crearemos el archivo de configuración para que Docker Compose gestione Portainer.

Crea una carpeta para Portainer y accede a ella:

```bash
mkdir ~/portainer
cd ~/portainer
```
Crea el archivo docker-compose.yml:
```
nano docker-compose.yml
```
Pega el siguiente contenido (docker-compose.yml del repositorio) en el archivo. Este archivo define cómo se debe ejecutar Portainer.

Guarda los cambios y cierra el editor (Ctrl+X, luego Y, y Enter).

## Paso 2: Iniciar Portainer
Con el archivo de configuración listo, levanta el servicio con un solo comando.

Ejecuta Docker Compose en modo "detached" (en segundo plano):
```
docker compose up -d
```
Docker descargará la imagen de Portainer y la iniciará con la configuración que definiste.

Verifica que el contenedor esté en ejecución:

```
docker ps
```
Deberías ver un contenedor llamado portainer en la lista.

## Paso 3: Acceso y Configuración Inicial
Abre tu navegador web y ve a la dirección de tu Raspberry Pi usando HTTPS y el puerto 9443:

https://< IP-DE-TU-RASPBERRY-PI >:9443

Ejemplo: https://192.168.100.50:9443 

Tu navegador mostrará una advertencia de seguridad. Esto es normal. Haz clic en "Avanzado" y "Continuar al sitio".

En la primera pantalla, crea tu usuario administrador estableciendo un nombre de usuario y una contraseña segura.

A continuación, selecciona "Get Started" para gestionar el entorno Docker local donde se está ejecutando Portainer.

¡Listo! Ya tienes acceso completo al panel de Portainer para gestionar tus contenedores de forma gráfica.