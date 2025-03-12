# Practica 8
## Victor Gabriel Bojorges Hermosillo
### 1. ¿Cómo se inicializa un repositorio en Git?
Para inicializar primero se debera introducir la cuenta de github con usuario y correo y con el comando "Git init" y a partir de ahí poder usarlo (en VSC).
En Github Desktop o Browser igual el proceso es iniciar sesión y abrir el repositorio directamente.
 
```bash
Ejemplo en Visual Studio Code:

git config --global user.name (Nombre de usuario)
git config --global user.email (Correo de Github)
Git init (Iniciar Repositorio)
```
### 2. ¿Cómo creas un repositorio en GitHub?
En Github se puede crear un repositorio con un botón que te crea el tipo de repositorio que desees, Puede ser Publico o Privado y una vez creado se puede accesar, En Desktop se puede crear de forma local para despues subirse a su propio repositorio.
```bash
En GitHub Desktop 
 + Create a New Repository on your local drive (Crear un repositorio desde la computadora)

 En Github Browser 

 - Create a new repository  
```
### 3. ¿Cómo vinculas un repositorio local de Git con uno remoto en GitHub?
En Git para vincular se debe insertar una serie de codigos tanto para crear el repositorio como para vincularse.
Para hacerlo debe hacerse el mismo paso de iniciar sesión pero ahora se debe ingresar el repositorio destino al cual se va a enviar todo.
```bash
Para vincular un repositorio existente
git branch -M main
git remote add origin (Link del repositorio)
git push -u origin main 
```
### 4. ¿Cuál es el flujo básico de trabajo en Git y GitHub?
El flujo de trabajo sirve para subir los archivos de tal modo que Git tenga conocimiento de estos archivos y el seguimiento que les dara para subirlos al repositorio hasta que el usuario los suba
```bash
Para añadir y subir los archivos 
git add . (para añadir el archivo para hacer commit)
git commit -m ""(nombre del commit entre las comillas)
git push (para subir el archivo)
```
### 5. ¿Para qué sirve el archivo .gitignore?
El archivo .gitignore sirve para que en el repositorio al momento de subirse ignore el tipo de archivo que se especifique para que no lo incluya, por ejemplo archivos .exe, .md, entre muchos otros.
```bash
para crear el archivo .gitignore y especificarle los archivos a ignorar
touch .gitignore 

(Una vez en el archivo)
*.exe 
```
### 6. ¿Cuál es el propósito de una rama?
La rama sirve para crear una linea del tiempo en donde los cambios que se hagan estarán en un nuevo espacio donde no afectaran a la rama de la cual se separaron, por lo cual se duplica y ahora se puede trabajar en este nuevo espacio para no afectar al anterior.
```bash
Crear una Rama
git branch (Nombre de la rama) (Para crear la rama)
git checkout (Nombre de la rama) (Para moverse a la rama creada)
```
### 7. ¿Qué es una fusión?
La fusion sirve para juntar los cambios que se hicieron en las ramas y juntar su información para que este actualizada con la rama que se desea fusionar, esto sirve para juntar informacion que puede ser colaborativa y tenerla junta sin necesidad de copiar y pegar manualmente.
```bash
Fusion de Ramas 
git checkout (El nombre de la rama que se desea juntar la información)
git merge (Nombre de la rama donde se sacara el contenido y se juntara)
```
### 8. Explica los diferentes tipos de fusión que existen.
Hay 2 tipos de fusiones en las cuales una la hace de forma rapida y no tiene contenido que pueda interferir con lso archivos originales y el segundo es que cuando se detecta contenido que pueda estar chocando y editarlo manualmente.
### 9. ¿Cómo puedes ver el historial de tu repositorio?
Se pueden ver de varias formas pero las mas comunes son:
```bash
git log --oneline (Da un listado de los documentos mas rapido)
git log (Te da de forma detallada cada modificacion que se hizo)
git log > commits.txt (Crea un archivo donde se muestran los cambios incluidas las ramas creadas)
```
### 10. ¿Cuál es el propósito de una etiqueta?
Las etiquetas sirven para determinar que version del software que se esta desarrollando y como va cambiando constantemente.
Un ejemplo seria la Version 1.1.0 
La primera linea es la version mas pesada y que contiene elementos importantes para el programa.
La segunda linea sirve para decir que contiene elementos que son importantes pero que no necesariamente son mas grandes para poder reemplazar el archivo principal.
La tercera linea sirve para determinar parches que son para cambios menores como reparacion de bugs y glitches.
```bash
git tag v1.0.0 (Para crear la etiqueta)
git add . 
git commit -m "v1.1.0"
git push --tags (para subir la etiqueta)
```