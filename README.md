Para obtener el token de Tailscale, basta con crear una cuenta, dirigirte al apartado de settings, key y en la sección de Auth keys, gerenamos una.

Preparación del entorno
Cree un directorio para el proyecto:

```
mkdir navidrome-tailscale && cd navidrome-tailscale
```
Cree la estructura de carpetas necesaria para los volúmenes:
```
mkdir -p navidrome/data navidrome/music navidrome/tailscale-lib
```

```
mkdir  tailscale-navidrome
```

Crea un archivo llamado docker-compose.yml y pegue el contenido del servicio proporcionado.

Jerarquia de directorios
```
├──docker-compose.yml
├── navidrome
│    ├── data
│    └── music
│    └──tailscale-lib
└── tailscale-navidrome
```
Acceso al servicio:

Debido a que Navidrome utiliza el modo de red service:tailscale, el contenedor de música comparte la interfaz de red de Tailscale.
Busca la dirección IP asignada o el nombre de host (melon) en el panel de Tailscale.

Acceda a la interfaz web desde cualquier dispositivo conectado a su red Tailscale utilizando el puerto por defecto de Navidrome (4533):
```
http://melon:4533
```
```
http://<IP-DE-TAILSCALE>:4533
```
