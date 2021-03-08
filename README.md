# TrabajoUnidad2
Laboratorio de Docker para realizar pruebas de vulnerabilidades sobre OWASP Mutillidae

# Conjunto de Script's de preparación del laboratorio local 
Este repositorio contiene los scripts necesarios para la instalación y confugración de un ambiente local de Dockers, además de poder realizar la habilitación de una maquina virtual Linux preconfigurada con el software web Mutillidae II para realizar análisis y pruebas de vulnerabilidades sobre este ambiente.

# Por favor siga los pasos a continuación para preparar el ambiente

### Empecemos 

Clonar el repositorio y uso del script bash pentestlab.sh como se describe a continuación en la consola shell (teclas rápidas Crtl+Alt+T) o buscar en la barra de menu de kali el icono Terminal y hacer clic sobre él. 
```
Ejecutamos el comando siguiente para descargar nuestro repositorio en nuestra carpeta HOME del usuario Kali
git clone https://github.com/itboxltda/pentestlab.git
cd pentestlab

# Procedemos a instalar el sistema Docker's en nuestro Kali Linux 
# ejecute el siguiente comando, este le solicitará la contraseña del usuario Kali para su ejecución (contraseña: Kali) y nos solicitará la confirmación (Yes/Si)  

./install_docker_kali_x64.sh

# descargar y ejecutar la máquina virtual de Mutillidae II 
./pentestlab.sh start mutillidae
# ... para descargar la imagen de mutillidae docker y mapearla a nivel del host local en la siguiente url http://mutillidae

# Imprima una lista completa de proyectos disponibles use el comando list
./pentestlab.sh list 

# Ejecutar el script sin comandos imprimirá información de ayuda
./pentestlab.sh 
```


### comandos disponibles
```
uso general: ./pentestlab.sh {list|status|info|start|stop} [nombredelproyecto]

 Este script usa Docker y alias de hosts para hacer que las aplicaciones web estén disponibles en localhost"

ejemplos de los comandos

./pentestlab.sh list
Lista de todos los proyectos disponibles   

./pentestlab.sh status
Mostrar el estado de todos los proyectos
   
./pentestlab.sh start mutillidae
   Inicio del contenedor con la aplicación web mutillidae y dejarlo disponible de manera local
   
./pentestlab.sh stop mutillidae
   Detener contenedor docker

./pentestlab.sh info mutillidae
   Mostrar información sobre el proyecto mutillidae 
```

 ### Referencia a archivos Dockers para el contenedor de Mutillidae y el repositorio de su creador 
 Mutillidae II		- Nikolay Golub (citizenstig/nowasp)  
