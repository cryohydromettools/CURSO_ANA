# Ambiente de desarrollo integrado (IDE)

Un entorno de desarrollo integrado (IDE, sigla en inglés), es una aplicación informática que proporciona servicios integrales para facilitarle al desarrollador o programador el desarrollo de un software o aplicacón. Muchos IDEs están disponibles. Sin embargo, en este módulo enseñaremos cómo instalar Jupyter-lab y Visual Studio Code. La mayor parte del curso será dado usando Visual Studio Codo pero **siéntase libre** de elegir el IDEs más confortable para usted.

## Linux

No todos los sistemas operativos linux tienen estos aplicativos en sus tiendas **on-line** por lo que se recomienda el uso del terminal.

### JupyterLab

1. Mediante el uso `pip`
```bash
pip install jupyterlab
```
Normalmente el proceso de instalación no demora, para abrirlo debemos utilizar colocar el siguiente comando en el terminal:

```bash
jupyter-lab
```
Esto nos abrira una nueva aba en el navegador.

![Jupyter-lab con pip](./figs_linux/jupyter_lab.png)

Si desea desinstalar use el siguiente comando:

```bash
pip uninstall jupyterlab
```

2. Mediante el uso de `conda`

```bash
conda install -c conda-forge jupyterlab
```
Este procedimiento normalmente demora un poco. Despues de un momento retornará un mensaje preguntando si deseamos continuar con la instalación de algunas librerias necesarias. Escriba `y` o simplemente presiones `enter`.

![Jupyter-lab con conda](./figs_linux/conda_jupyter.png)

La instalación debe concluir sin errores. Para inicilizar el escriba en el terminal:

```bash
jupyter-lab
```
Este comando abrirá una nueva aba del navegador con el ambiente de desarrolo `jupyter-lab`, de forma semejando al instalado por el `pip`.
![Abrir jupyter-lab](./figs_linux/jupyter_lab.png)

El proceso de desinstalación es realizado con el comando:

```bash
conda remove jyupyterlab
```
### Visual Studio Code

Este es un IDE desarrollado por la Microsoft, puedes descargar este programa desde la pagina de [descarga-vscode](https://code.visualstudio.com/download). Se mostraran las versiones disponibles para algunos sistemas operativos (linux, windows e mac).

1. Instalación manual
- Descarga paquete adecuado con tu sistema operativo (deb, rpm).
- Para usuarios ubuntu:
```bash
sudo apt update
sudo apt install ./<file>.deb
```
- Esto actualizara los permisos y fuentes de distribución.
- Una vez concluido debes ejecutar el siguiente comando:

```bash
sudo apt install apt-transport-https
sudo apt update
sudo apt install code
```

2. Via snap, para esto se recomiendo utilizar los siguientes comandos:
Instalar inicialmente el `app store` de linux [snap](https://snapcraft.io/). Por ejemplo en el Ubuntu debes ejecutar los comandos:

```bash
sudo apt update
sudo apt install snapd
```

Una vez instalado el `snap` utiliza el siguiente comando:

```bash
sudo snap install code --classic
```

- Puedes iniciar este programa buscandolo por el iniciador de programas, el cual debe abrir una ventana como esta:

![Visual code](./figs_linux/vscode_inst.png)


