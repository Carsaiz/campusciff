#CARLOS SAIZ ALVES

##2. EJERCICIOS

###2.1. REPOSITORIO CAMPUSCIFF

####2.1.1. Crear un repositorio llamado campusciff en nuestro GitHub

git config --global user.name "Carsaiz"

git config --global user.email "carlos_sa_620@hotmail.com"

cd campusciff  (ya había sido creado en clase)

git init

####2.1.2. Clonar repositorio en el local.

(Primero generar una clave SSH)

cd ~/.ssh

ssh-keygen

cat ~/.ssh/id_rsa.pub 

git init   (Para inicializar la carpeta) 

git clone https://github.com/carsaiz/campusciff  (Clonar el repositorio) 

####2.2.1. Cear en el local, un archivo README.md

ls

cd repogit

cd campusciff

touch README.md  

echo para copiar lo que esta en el .txt a README

###2.3. COMMIT Y PUSH inicial

####2.3.1. Añadir los comandos utilizados hasta ahora y hacer un commit inicial con el mensaje commit inicial

git commit -m "commit inicial"

####2.3.2. Subir los cambios a un repositorio remoto

git pull

git push https://github.com/carsaiz/campusciff master

###2.4. IGNORAR ARCHIVOS

####2.4.1. Crear en el repositorio local fichero llamado privado.txt

touch privado.txt

####2.4.2. Crear en el repositorio local una carpeta llamada privada.

mkdir privada

####2.4.3. Realizar los cambios oportunos para que sean ignorados por git.

touch .gitignore

cat .gitignore

gedit .gitignore ( instalarlo con sudo apt-get install gedit # abrirlo y escribir: privado.txt y /privada en la otra linea )

git add .gitignore

git commit -m "Creación del archivo oculto"

###2.5 CREAR EL TAG V0.1

####2.5.1. Añadir fichero 1.txt al repositorio local.

touch 1.txt

####2.5.2. Crear un tag v0.1.

git tag -a v0.1 -m "Tag creado"

####2.5.3. Subir los cambios al repositorio remoto.

git add 1.txt

git push https://github.com/carsaiz/campusciff master

###2.6 CREAR UNA RAMA REMOTA V0.2

####2.6.1. Crear una rama remota v0.2.

git branck v0.2

####2.6.2. Posiciona tu carpeta de trabajo en esta rama.

git checkout v0.2

####2.6.3. Añadir un fichero 2.txt en la rama v0.2.

touch 2.txt

####2.6.4. Subir los cambios al reposiorio remoto.

git add 2.txt

git commit -m "creado el archivo 2.txt"

git push https://github.com/carsaiz/campusciff v0.2

###2.7 MERGE DIRECTO

####2.7.1. Posicionarse en la rama master.

git chechout master

####2.7.2. Hacer un merge de la rama v0.2 en la rama master

git merge v0.2

###2.8 MERGE CON CONFLICTO

####2.8.1. En la rama master poner Hola en el fichero 1.txt y hacer commit

vi 1.txt  (para editar el fichero 1.txt y ahí pongo Hola y para salir de ese editor :qb)

git add 1.txt

git commit -m "Hola puesto en el fichero 1.txt"

####2.8.2. Posicionarse en la rama v0.2 y Adios en el fichero "1.txt" y hacer commit

git checkout v0.2 (para ponernos en la rama v0.2)

vi 1.txt (y pongo Adios y para salir :qb)

git add 1.txt

git commit -m "Adios puesto en el fichero 1.txt de la rama v0.2)

####2.8.3. Posicionarse de nuevo en la rama master y hacer un merge con la rama v0.2

git checkout master (para volver a la rama master)

git merge v0.2

####2.8.4. Listar las ramas con merge y las ramas sin merge.

git branch --merged

git branch --no-merged

####2.8.5. Arreglar el conflicto anterior y hacer un commit.

git status

git diff

vi 1.txt (para editar que Hola y Adios no estén en la misma línea y :qb para salir)

git add 1.txt

git commit -a

###2.9 BORRAR RAMA

####2.9.1. Crear un tag v0.2

git tag -a v0.2 -m "Etiqueta creada"

####2.9.2. Listar los distintos commits con sus ramas y sus tags

git tag -n

####2.9.3. Borrar la rama v0.2

git branch -d v0.2

###2.10 CUENTA DE GITHUB

####2.10.2 Poner el doble factor de autentificación

![Creative Commons BY SA](Captura de pantalla 2015-11-21 a la(s) 14.48.30)

###2.12 CREAR UNA TABLE

|NOMBRE          |GITHUB                                            |
|:---------------|:-------------------------------------------------|
|Antonio Bastidas|[Antonio Bastidas](https://github.com/Antonio2106)|




