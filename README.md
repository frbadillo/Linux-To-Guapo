# Linux to' guapo

## ls (List)
**Opciones:**
- `-l`: Formato largo
- `-a`: Mostrar ocultos
- `-h`: Tamaños legibles
- `-R`: Recursivo
- `-t`: Ordenar por tiempo
- `-S`: Ordenar por tamaño

**Uso:** Listar contenido de directorios
```bash
# Listar todo en formato largo
ls -la

# Listar archivos ordenados por tamaño
ls -lSh
```

## cd (Change Directory)
**Opciones:**
- `..`: Directorio superior
- `-`: Directorio anterior
- `~`: Directorio home

**Uso:** Navegar entre directorios
```bash
# Ir a directorio superior
cd ..

# Volver a home
cd ~
```

## pwd (Print Working Directory)
**Opciones:**
- `-L`: Mostrar path con symlinks
- `-P`: Mostrar path físico

**Uso:** Mostrar directorio actual
```bash
# Mostrar ruta actual
pwd

# Mostrar ruta física
pwd -P
```

## mkdir (Make Directory)
**Opciones:**
- `-p`: Crear padres si no existen
- `-m`: Establecer permisos
- `-v`: Verbose

**Uso:** Crear directorios
```bash
# Crear directorio
mkdir proyectos

# Crear estructura completa
mkdir -p proyectos/src/js
```

## rm (Remove)
**Opciones:**
- `-r`: Recursivo
- `-f`: Forzar
- `-i`: Interactivo
- `-v`: Verbose

**Uso:** Eliminar archivos y directorios
```bash
# Eliminar archivo
rm archivo.txt

# Eliminar directorio y contenido
rm -rf directorio/
```

## cp (Copy)
**Opciones:**
- `-r`: Recursivo
- `-p`: Preservar atributos
- `-v`: Verbose
- `-i`: Interactivo

**Uso:** Copiar archivos y directorios
```bash
# Copiar archivo
cp origen.txt destino.txt

# Copiar directorio completo
cp -r /src /backup
```

## mv (Move)
**Opciones:**
- `-f`: Forzar
- `-i`: Interactivo
- `-u`: Update
- `-v`: Verbose

**Uso:** Mover o renombrar archivos
```bash
# Renombrar archivo
mv viejo.txt nuevo.txt

# Mover archivo
mv archivo.txt /destino/
```

## grep (Global Regular Expression Print)
**Opciones:**
- `-i`: Ignorar mayúsculas
- `-r`: Recursivo
- `-v`: Invertir coincidencia
- `-n`: Mostrar número de línea

**Uso:** Buscar patrones en archivos
```bash
# Buscar en archivo
grep "error" log.txt

# Buscar recursivamente
grep -r "TODO" ./src/
```

## ps (Process Status)
**Opciones:**
- `-e`: Todos los procesos
- `-f`: Formato completo
- `-u`: Por usuario
- `aux`: Todos los procesos detallados

**Uso:** Listar procesos en ejecución
```bash
# Ver todos los procesos
ps aux

# Procesos de usuario
ps -u usuario
```

## top (Table of Processes)
**Opciones:**
- `-u`: Filtrar por usuario
- `-p`: Filtrar por PID
- `-n`: Número de iteraciones
- `-b`: Modo batch

**Uso:** Monitor de procesos en tiempo real
```bash
# Monitor básico
top

# Procesos de usuario específico
top -u usuario
```

## df (Disk Free)
**Opciones:**
- `-h`: Formato legible
- `-T`: Mostrar tipo filesystem
- `-i`: Mostrar inodos
- `-l`: Solo locales

**Uso:** Mostrar espacio en disco
```bash
# Espacio en formato legible
df -h

# Mostrar tipo de filesystem
df -T
```

## cat (Concatenate)
**Opciones:**
- `-n`: Numerar líneas
- `-b`: Numerar líneas no vacías
- `-A`: Mostrar caracteres especiales
- `-s`: Suprimir líneas vacías repetidas

**Uso:** Mostrar contenido de archivos
```bash
# Ver contenido
cat archivo.txt

# Numerar líneas
cat -n archivo.txt
```

## ping
**Opciones:**
- `-c`: Número de paquetes
- `-i`: Intervalo
- `-s`: Tamaño de paquete
- `-w`: Timeout

**Uso:** Probar conectividad de red
```bash
# Ping básico
ping google.com

# 5 paquetes con intervalo 2s
ping -c 5 -i 2 8.8.8.8
```

## wget
**Opciones:**
- `-O`: Nombre de salida
- `-c`: Continuar descarga
- `-r`: Recursivo
- `-b`: Background

**Uso:** Descargar archivos de internet
```bash
# Descargar archivo
wget https://ejemplo.com/archivo.zip

# Continuar descarga interrumpida
wget -c https://ejemplo.com/archivo.zip
```
## ss (Socket Statistics)
**Opciones:**
- `-n`: Muestra números de puerto en vez de nombres
- `-t`: Solo conexiones TCP
- `-u`: Solo conexiones UDP
- `-l`: Solo sockets en escucha
- `-p`: Muestra proceso usando el socket
- `-a`: Todos los sockets

**Uso:** Examinar conexiones de red y estadísticas de sockets
```bash
# Ver todas las conexiones TCP
ss -t

# Ver sockets en escucha con procesos
ss -tlnp

# Filtrar por puerto
ss sport = :80
```

## ip
**Opciones:**
- `link`: Interfaces de red
- `addr`: Direcciones IP
- `route`: Tabla de enrutamiento
- `neigh`: Tabla ARP
- `-br`: Formato breve
- `-c`: Salida en color

**Uso:** Configuración y monitoreo de red
```bash
# Mostrar interfaces
ip link show

# Configurar IP
ip addr add 192.168.1.10/24 dev eth0

# Agregar ruta
ip route add default via 192.168.1.1
```

## curl
**Opciones:**
- `-X`: Método HTTP
- `-H`: Headers
- `-d`: Datos POST
- `-o`: Output a archivo
- `-L`: Seguir redirecciones
- `-v`: Verbose

**Uso:** Transferencia de datos y pruebas HTTP
```bash
# GET request
curl https://api.ejemplo.com

# POST con JSON
curl -X POST -H "Content-Type: application/json" \
     -d '{"nombre":"juan"}' https://api.ejemplo.com
```

## tcpdump
**Opciones:**
- `-i`: Interfaz
- `-n`: No resolver nombres
- `-w`: Escribir a archivo
- `-r`: Leer de archivo
- `-X`: Mostrar contenido hex/ASCII
- `-v`: Verbose

**Uso:** Captura y análisis de paquetes de red
```bash
# Captura básica
tcpdump -i eth0

# Filtrar por host y puerto
tcpdump 'host 192.168.1.1 and port 80'
```

## chmod
**Opciones:**
- Numéricas: 4(r), 2(w), 1(x)
- Simbólicas: u(user), g(group), o(others), a(all)
- `-R`: Recursivo
- `-v`: Verbose

**Uso:** Cambiar permisos de archivos
```bash
# Permisos totales
chmod 777 archivo.txt

# Agregar ejecución
chmod +x script.sh
```

## chown
**Opciones:**
- `-R`: Recursivo
- `-h`: Afectar enlaces simbólicos
- `-v`: Verbose
- `--reference`: Usar permisos de otro archivo

**Uso:** Cambiar propietario/grupo de archivos
```bash
# Cambiar propietario
chown usuario:grupo archivo

# Cambiar recursivamente
chown -R www-data:www-data /var/www
```

## apt
**Opciones:**
- `install`: Instalar paquetes
- `remove`: Eliminar paquetes
- `update`: Actualizar lista
- `upgrade`: Actualizar sistema
- `search`: Buscar paquetes
- `show`: Información de paquete

**Uso:** Gestión de paquetes Debian/Ubuntu
```bash
# Actualizar sistema
apt update && apt upgrade

# Instalar paquete
apt install nginx
```

## dpkg
**Opciones:**
- `-i`: Instalar paquete
- `-r`: Eliminar paquete
- `-l`: Listar paquetes
- `-s`: Estado de paquete
- `-L`: Listar archivos de paquete
- `-P`: Purgar paquete

**Uso:** Gestión de paquetes .deb
```bash
# Instalar .deb
dpkg -i paquete.deb

# Listar paquetes instalados
dpkg -l | grep nginx
```

## aptitude
**Opciones:**
- `install`: Instalar paquetes
- `remove`: Eliminar paquetes
- `search`: Buscar paquetes
- `show`: Mostrar información
- `update`: Actualizar lista
- `upgrade`: Actualizar sistema

**Uso:** Interfaz avanzada para gestión de paquetes
```bash
# Buscar paquete
aptitude search nginx

# Instalar con resolución de dependencias
aptitude install postgres
```
