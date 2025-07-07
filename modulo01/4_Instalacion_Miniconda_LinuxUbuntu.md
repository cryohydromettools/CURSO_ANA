# 1. Instalación de Miniconda en Linux Ubuntu

## 1.1 ¿Qué es Miniconda?
Miniconda es una versión minimalista de Anaconda que incluye:
- Gestor de paquetes `conda`
- Intérprete Python
- Paquetes esenciales

### 1.1.1 Ventajas para Linux Mint
- No afecta al Python del sistema
- Permite múltiples entornos aislados
- Ideal para proyectos científicos

![Componentes de instalación](https://www.fabriziomusacchio.com/assets/images/posts/miniconda_thumb.jpg)

## 2. Requisitos previos

### 2.1 Verificar sistema
```bash
# Ejecutar en terminal:
lsb_release -a
uname -m
```

### 2.2 Dependencias necesarias
```bash
sudo apt update
sudo apt install libgl1-mesa-glx libegl1-mesa libxrandr2 libxrandr2 libxss1 libxcursor1 libxcomposite1 libasound2 libxi6 libxtst6
```

## 3. Descarga del instalador

### 3.1 Obtener última versión
```bash
wget https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh -O ~/miniconda.sh
```

### 3.2 Verificar integridad
```bash
sha256sum ~/miniconda.sh
# Comparar con el hash publicado en https://docs.conda.io/en/latest/miniconda.html
```

## 4. Proceso de instalación

### 4.1 Ejecutar instalador
```bash
bash ~/miniconda.sh
```

### 4.2 Siguiente el asistente
1. **Licencia**: Presionar `Enter` para avanzar y luego `yes` para aceptar
2. **Ubicación**: `/home/tu_usuario/miniconda3` (recomendado)
3. **Inicialización**: Responder `yes` para configurar el PATH

### 4.3 Finalizar instalación
```bash
source ~/.bashrc
```

## 5. Configuración inicial

### 5.1 Actualizar conda
```bash
conda update conda
```

### 5.2 Configurar canales
```bash
conda config --add channels conda-forge
conda config --set channel_priority strict
```

### 5.3 Crear primer entorno
```bash
conda create --name mint_env python=3.10
conda activate mint_env
```

## 6. Integración con el sistema

### 6.1 Acceso rápido desde terminal
Agregar al final de `~/.bashrc`:
```bash
alias condaenv="conda activate mint_env"
```

### 6.2 Desinstalación (si es necesario)
```bash
rm -rf ~/miniconda3
# Eliminar líneas relacionadas en ~/.bashrc
```

## 7. Uso práctico

### 7.1 Comandos esenciales
```bash
# Listar entornos
conda env list

# Instalar paquetes
conda install numpy pandas matplotlib

# Exportar entorno
conda env export > environment.yml
```

### 7.2 Ejemplo: Entorno para ciencia de datos
```bash
conda create --name datascience python=3.9
conda activate datascience
conda install jupyter numpy pandas scikit-learn seaborn
```

## 8. Solución de problemas

### 8.1 Error: "Command not found"
```bash
export PATH=~/miniconda3/bin:$PATH
source ~/.bashrc
```

### 8.2 Conflictos de paquetes
```bash
conda clean --all
conda update --all
```

### 8.3 Restablecer configuración
```bash
conda config --remove-key channels
```
