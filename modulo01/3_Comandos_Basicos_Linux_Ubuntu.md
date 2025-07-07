# Comandos Básicos de Linux Mint

![Logo Ubuntu](https://assets.ubuntu.com/v1/29985a98-ubuntu-logo32.png)

## 1. Introducción
Este notebook contiene los comandos esenciales para comenzar a usar Linux Mint, organizados por categorías con ejemplos prácticos.

## 2. Comandos del Sistema

### 2.1 Información del sistema
```bash
# Versión sistema
lsb_release -a

# Versión del kernel
uname -r

# Tiempo de actividad del sistema
uptime
```

### 2.2 Gestión de paquetes
```bash
# Actualizar lista de paquetes
sudo apt update

# Actualizar paquetes instalados
sudo apt upgrade

# Instalar un programa
sudo apt install nombre_paquete

# Eliminar un programa
sudo apt remove nombre_paquete
```

## 3. Manejo de Archivos y Directorios

### 3.1 Navegación
```bash
# Mostrar directorio actual
pwd

# Listar archivos (detallado)
ls -l

# Cambiar de directorio
cd /ruta/directorio

# Volver al home
cd ~
```

### 3.2 Manipulación de archivos
```bash
# Copiar archivo
cp origen destino

# Mover/renombrar
mv viejo nuevo

# Eliminar archivo
rm archivo

# Crear directorio
mkdir nombre_directorio
```

## 4. Procesos y Usuarios

### 4.1 Gestión de procesos
```bash
# Mostrar procesos en ejecución
top

# Versión simplificada
htop

# Matar proceso
kill PID
```

### 4.2 Usuarios y permisos
```bash
# Cambiar permisos
chmod 755 archivo

# Cambiar propietario
sudo chown usuario:grupo archivo

# Añadir usuario
sudo adduser nombre_usuario
```

## 5. Red y Conexiones

### 5.1 Configuración de red
```bash
# Dirección IP
ip a

# Conexiones activas
ss -tulnp

# Prueba de conectividad
ping google.com
```

### 5.2 SSH y transferencias
```bash
# Conectar por SSH
ssh usuario@direccion_ip

# Copiar archivos remotos (SCP)
scp usuario@host:archivo local
```

## 6. Búsquedas y Texto

### 6.1 Buscar archivos
```bash
# Buscar por nombre
find /ruta -name "*.txt"

# Buscar contenido
grep "texto" archivo
```

### 6.2 Manejo de texto
```bash
# Ver contenido
cat archivo.txt

# Ver por páginas
less archivo.txt

# Contar líneas
wc -l archivo.txt
```

## 7. Atajos Útiles

```bash
# Limpiar terminal
clear

# Historial de comandos
history

# Ejecutar comando anterior con sudo
sudo !!

# Autocompletar con TAB
# Escribir primeras letras y presionar TAB
```

## 8. Prácticas Recomendadas

1. **Usar sudo con cuidado**: Solo cuando sea necesario
2. **Actualizar regularmente**: `sudo apt update && sudo apt upgrade`
3. **Hacer backups**: De archivos importantes
4. **Documentar cambios**: En archivos de configuración
5. **Probar comandos**: Antes de ejecutarlos en producción


```python

```
