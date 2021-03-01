

# INSTALACIÓN CONDA Y EJECUCIÓN DE SPYDER

# Autor: Rafael Egea Jurado



## 1. Entorno spyder

Para esto, primero instalamos anaconda3 de acuerdo a las indicaciones del sitio web:  _Installing on Linux — Anaconda documentation_(2021).

1. Instalamos dependencias necesarias:
   
	`apt-get install libgl1-mesa-glx libegl1-mesa libxrandr2 libxrandr2 libxss1 libxcursor1 libxcomposite1 libasound2 libxi6 libxtst6`

2. Descargamos el instalador de anaconda de la siguiente pagina. [Página descargar](https://www.anaconda.com/products/individual#linux)

3. Introducimos el siguiente comando (Si lo tenemos en la carpeta _Downloads_):

	`bash ~/Downloads/Anaconda3-2020.02-Linux-x86_64.sh`
	
4. A continuación introducimos todo los que nos va pidiendo el instalador.

5. Una vez que ya lo tenemos instalado. Debemos configurar nuestro **PATH** mediante el siguiente comando en nuestro caso específico.

	 `export PATH="$PWD/anaconda3/bin:$PATH"`

6. Una vez tenemos esto realizado. Podemos ejecutar el siguiente comando

	`conda list` Para ver los paquetes ligados al entorno de conda
	
	
## 2. Ejecución de spyder

 `conda list | grep spyder` Podemos ejecutar este comando para ver si tenemos spyder instalado.

Ya que tenemos conda instalado y nos hemos asegurado que esta el paquete spyder. Podemos arrancarlo mediante el siguiente comando.

`conda run spyder`
	
	


## Bibliografía

- _Installing on Linux — Anaconda documentation._ (2021). (https://docs.anaconda.com/anaconda/install/linux/)
