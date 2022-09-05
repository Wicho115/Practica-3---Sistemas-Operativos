# Git Bash

## Comandos
1. pwd
   - sirve para saber donde esta posicionada la consola de comandos
   ```bash
   pwd -W
   >>> C:/Users/Dante
   ```
1. whoami
   - Te dice el usuario que está usando la terminal
   ```bash
   whoami
   >>> Dante
   ```
1. help
   - ayuda a saber que comandos puedes usar
   - puedes ver las banderas de comandos colocando el comando despues de help
   ```bash
   help
   help [COMMAND]
   [COMMAND] --help
   ```
1. clear
   - Sirve para limpiar la pantalla de comandos
   ```bash
   clear
   ```
1. ls
   - Sirve para listar todos los directorios y archivos en el directorio actual
   ```bash
   ls
   >>> SomeDirectory/ foo.txt bar.pdf
   ```
1. cd
   - Comando que te ayuda a cambiar entre directorios
   ```bash
   pwd -W
   >>> C:/
   cd "Program Files"
   >>> C:/Program Files
   ```
1. touch
   - puedes generar archivos con la extension quieras
   ```bash
   touch HolaMundo.txt
   ls
   >>> HolaMundo.txt
   ```
1. echo
   - puedes generar un archivo pero con texto en el archivo.
   ```bash
   echo "Hola estudiantes de amerike" > Hola.txt
   ```
1. cat
   - Puedes leer como respuesta en termial el contenido de un archivo.
   ```bash
   cat Hola.txt
   >>> "Hola Estudiantes de amerike"
   ```
1. mkdir
   - Crea un directorio
   ```bash
   mkdir Documentos
   ls
   >>> Documentos/ HolaMundo.txt Hola.txt
   ```
1. rmdir
   - Solo puede eliminar directorios vacios
   ```bash
   ls
   >>> SomeEmptyDirectory/ HolaMundo.txt
   rmdir SomeEmptyDirectory/
   ls
   >>> HolaMundo.txt
   ```
1. rm
   1. -r
      - Elimina directorios enteros (Tienen que estar cerrados)
      ```bash
      ls
      >>> ClosedDirectory/ HolaMundo.txt
      rm -r ClosedDirectory 
      ls
      >>> HolaMundo.txt
      ```
   2. -rf
      - Elimina directorios enteros (Sin necesidad de estar cerrados)
      ```bash
      ls
      >>> OpenDirectory/ HolaMundo.txt
      rm -rf OpenDirectory 
      ls
      >>> HolaMundo.txt
      ```
1. cp
   - Copias el archivo de origen al nuevo directorio, puede cambiarle el nombre si gustas
   ```bash
   cp HolaMundo.txt Documentos/HolaMundo.txt
   cd Documentos
   ls
   >>> HolaMundo.txt
   ```

   1. -r
      - Sirve para copiar directorios enteros
      ```bash
      ls
      >>> Directory1/ Directory2/
      cp -r Directory1 Directory2
      cd Directory2
      ls
      >>> Directory1/ SomeDir2File.txt
      ```
1. mv
   - Mover archivos y directorios, igualmente puedes editar nombres de archivos
   ```bash
   ls
   >>> HolaMundo.txt Documentos/
   mv HolaMundo.txt Documentos/
   cd Documentos
   ls
   >>> HolaMundo.txt
   ```
1. find
   - Encuentra archivos y los imprime en la terminal, se pueden 
   ```bash
   find P*
   >>> Program/ Pepe/ Programa.txt
   ```
1. code
   - Abre el ditor de texto de visual studio code del directorio seleccionado
   ```bash
   code ./
   ```
<br>

# Comodines

Hay 6 comodines que se pueden usar para hacer más facil el manejo de datos

1. ~
   - Este comodin sirve para representar el directorio principal del sistema operativo
   ```bash
   cd ~
   >>> C:/Users/Dante
   ```
1. /
   - Este comodin sirve para representar la carpeta raíz del bash, generalmente es la raíz del disco en onde está instalado, pero puede ser la carpeta en donde se encuentre el bash portable
   ```bash
   cd /
   >>> C:/
   ```
1. .
   - El comodin punto sirve para representar el directorio actual
   ```bash
   cd . 
   >> C:/Projects
   ```
1. ..
   - Este comodin se usa junto al comando cd y es para poder subir 1 nivel en los directorios
   ```bash
   pwd -W
   >>> C:/Projects/src
   cd ..
   >>> C:/Projects
   ```
1. ""
   - Este comodin se usa para representar cadenas de tectos que tengan caracteres raros o espacios
   ```bash
   cd "Program Files"
   >>> C:/Program Files
   ```