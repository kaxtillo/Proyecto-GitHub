# Proyecto-GitHub

Descripción de comandos para la terminal de linux debian

git config --global user.name "xxxxxx" 
git config --global user.email "xxxxxx@xxxx.com"

Generando tu Public Key:

ssh-keygen

Leyendo tu llave para copiarla a Github:

cat ~/.ssh/id_rsa.pub

Arrancando tu proyecto:

git init

touch README

git add README

git commit -m "tu primer commit"

git push origin master

**********************

crea una copia local del repositorio ejecutando git clone /path/to/repository al utilizar un servidor remoto, el comando será git clone username@host:/path/to/repository

**********************

tu repositorio local esta compuesto por tres "árboles" administrados por git:

1.Directorio de trabajo el cual contiene los archivos. 
2. Index el cual actua como un área intermedia.
3. HEAD el cual apunta a el último commit realizado.

add & commit

Puedes proponer cambios (agregarlos a el Index) usando git add git add * Este es el primer paso en el flujo de trabajo básico. Para en realidad hacer commit a estos cambios usa git commit -m "Commit message" Ahora el archivo esta incluído en el HEAD, pero aún no en tu repositorio remoto.

envío de cambios

Tus cambios están ahora en el HEAD de tu copia local. Para enviar esos cambios a tu repositorio remoto ejecuta git push origin master Reemplaza master por la rama a la cual desees enviar tus cambios.

Si no has clonado un repositorio existente y quieres conectar tu repositorio a un repositorio remoto, necesitas agregarlo con git remote add origin Ahora puede subir tus cambios al repositorio remoto selecionado ramas Las ramas son utilizadas para desarrollar funcionalidades aisladas unas de otras. La rama master es la rama por "defecto" cuando creas un repositorio. Usa otras ramas para el desarrollo y fusionalas de regreso a la rama principal al terminar.

crea una nueva rama llamada "feature_x" y cambiate a ella usando:

git checkout -b feature_x regresa a la rama principal git checkout master y borra la rama git branch -d feature_x una rama no está disponible para los demás a menos que subas (push) la rama a tu repositorio remoto git push origin

actualiza & fusiona

para actualizar tu repositorio local al commit más nuevo, ejecuta git pull en tu directorio de trabajo fetch y merge cambios remotos. para fusionar otra rama a tu rama activa (por ejemplo master), utiliza git merge en ambos casos git intenta auto fusionar cambios. Desafortunadamente, esto no es posible todo el tiempo y resulta en conflictos. Tú eres responsable de fusionar esos conflictos manualmente al editar los archivos mostrados por git. Luego de modificarlos, necesitas marcarlos como fusionados con git add antes de fusionar cambios, también puedes dar un vistazo previo usando git diff
