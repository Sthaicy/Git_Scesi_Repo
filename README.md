# TRABAJO INDIVIDUAL

JHOSSELIN STHAICY BUSTAMANTE ESCOBAR

## Clase 1 
Es un sistema de control de versiones

###que es git?


### Subtitulo
para codigo colocar tres comillas 

```
sudo apt install git

```
Para imagenes debemos investigar

## CLASE 2

###STATES Y COMMITS

git gestiona cada archivo en 3 estados 
-directorio de trabajo
 carpeta comun haces tu codigo cosas , framework
 git no hace nada solo obseva lo que haces con UNTRACKED
 MODIFIED archivo que paso por las 3 fases pero realizamos un cambio
 cualquier archivo que no este en el git ignore pasa a esos estados

-stage area (git ve tus cambios)
-repositorio local(crea el punto de guardado)

git status → nos da los archivos con seguimiento y sin seguimiento 

-pero si realizas un cambio en el achivo creado se pasa a la parte de cambios no guardados

Que pasa si borramos un archivo?

En git status el archivo borrado entra en borrados
-stage area (git ve tus cambios)
-repositorio local(crea el punto de guardado)

-Cuando haces git init solo funciona en los archivos de  la capeta en dodne nos encontramos 

-El gitIgnore son archivos que no dara seguimiento y que tampoco podra ver GIT

```git restore <archivo>```

Ejemplo.-

git status → nos da los archivos con seguimiento y sin seguimiento 

-pero si realizas un cambio en el achivo creado se pasa a la parte de cambios no guardados

Que pasa si borramos un archivo?

En git status el archivo borrado entra en borrados
-stage area (git ve tus cambios)
-repositorio local(crea el punto de guardado)

-Cuando haces git init solo funciona en los archivos de  la capeta en dodne nos encontramos 

-El gitIgnore son archivos que no dara seguimiento y que tampoco podra ver GIT

git restore <archivo>

Si quiero que el archivo modificado regrese a su estado original pero cuidado esto borra fisicamente lo que escribimos, solo aplica para archivos que estuvieron en seguimiento

###Que pasa si  quiero que el archivo que cree en git  no se vea?

ejemplo → nano .env para guardar nuestras credenciales secretas 

pero al ver en status aun se ve y para configurar el archivo solo debo agregar su nombre dentro del archivo ‘gitignore’ 

-Tambien se puede usar expresiones regulares como en linux x como un comodin 

-Tambien funciona con carpetas “venv/” debe tener la barra al final para ignorar todo lo de adentro

```git add <nombre archivo>```

para poder anadir archivos dentro de mi gitignore

```git add .```

anade todos los archivos  

pero si quiero regresar atras solo debo usar el comando 

```git restore --staged README.md```

esto quita el archivo de staged y vuelve a modify

```git restor```

elimina fisicamente el cambio y si lo implementas en un archivo borrado vuelve a aparcer 

--Entrara en el examen que hace ‘’stage''

Es parar quitarlo de la parte stage y devolverlo en modifY, debemos colocar ese stage solo para dar un pasoo hacia atras , sino va descartar el cambio o va a recrear el archivo eliminado

###REPOSITORIO LOCAL CONFIRMADO 

Ultima fase parar decirle al repositorio que cree el punto de guardado

```git commit -m "Creado el gitignore"```

¡Perfecto! Aquí tienes todo en un solo bloque de texto, listo para copiar directamente:

```markdown
###Inicializar el repositorio y primer commit

```bash
nano README.md
cat README.md
git init
git add README.md   # añadir nuestro archivo al staging area
git commit -m "Primer commit"
git log   # muestra el historial de commits (autor, fecha, mensaje)
```

###Modificaciones y segundo commit

```bash
nano README.md
git add README.md
git commit -m "segundo commit"
git log
git status   # ver el estado de los archivos en el repositorio
```

###Crear y configurar .gitignore

```bash
touch .gitignore
git add .gitignore
git add .        # agregar todos los archivos al staging
git status
```

###Deshacer cambios del área de staging

```bash
git restore --staged README.md   # sacar README.md del staging
git status
```

###Probar git restore con un archivo nuevo

```bash
touch README_NUEVO.md
git add README_NUEVO.md
rm README_NUEVO.md                # eliminar archivo después de agregarlo
git restore README_NUEVO.md      # restaurar desde el último commit o staging
git add .
git commit -m "Creado el gitignore"
git log
```

###Ver historial de forma resumida

```bash
git log --oneline   # muestra cada commit en una sola línea
```

###Deshacer el último commit con git reset --soft

```bash
# Este comando hace que HEAD retroceda un punto de guardado
git reset --soft HEAD~1
git log
```

Nota importante: El commit que se deshace con `reset --soft` aún puede recuperarse si no se han hecho más cambios. Usar con cuidado.

###Buenas prácticas

- Cada cuanto hacemos un commit?  

-Que nombre debemos usar para los commits

-debemos hacer commits cortos , cambios cortos simples, cada que hagamos una mini tarea hacer un commit

-Como hacer buenos commits .- 

```git commit --amend -m "Creando el .gitignore"```

Es parar cambiar el nombre del commit  pero cambia el ide como si lo borrraramos y volvieramso a crear

- COMMITS ATOMICOS.- para cada funcion un commit 

- Los commits deben ser en ingles 

1.- Usar verbos imperativos (Add, change, Fix, Remove)

2.- No uses punto final ni puntos suspensivos en tus mensajes

3.- Usa coomo maximo 50 caracteres

4.- Usa un prefijo para tus commits

Prefijos:feat: para una nueva característica para el usuario.

fix: para un bug que afecta al usuario.

perf: para cambios que mejoran el rendimiento del 

sitio.build: para cambios en el sistema de build, tareas de despliegue o i

nstalación.ci: para cambios en la integración 

continua.docs: para cambios en la 

documentación.refactor: para refactorización del código como cambios de nombre de variables o 

funciones.style: para cambios de formato, tabulaciones, espacios o puntos y coma, etc; no afectan 

alusuario.test: para tests o refactorización de uno ya existente

- CADA QUE CREE MI DOCUMENTACION USAR DOC:

- Que pasa si le hago una funcionalidad tan grande que no es posible dividir como lo explicaria ?

usar :

git commit

se abrira editor de texto para crearr un titulo largo del commit

# TERCERA CLASE

###Crear la cuenta de github

-no con la institucional, porque te quitan al final de la carrera

debemos configurar el ssh con la llave ceada que debemos colocar en las configuraciones y anadimo el codigo geenrado para que git se conecte al git hub
Se puede mas de una llave pero nos dira la siguinete clase

### RECUARDA PARA GENERAR EL CODIGO 
```ssh-keygen -t ed25519 -C "sthaicy08@gmail.com"```
ENTRARA AL EXAMEN

si usamos http cada vez te pedira usuario y contrasena a cada rato para cada modificacion
- Si el git lo conectamos con el institucional nos dan bastentes beneficios un paqute de git

- el peso maximo en git es de 100 mg de subida , un limite de 10 gb el repositorio, para eso existe el gitignore para no subir cosas muy pesadas

- Se puede subir sin llave el codigo ?

Si se puede pero se sufre usando https , poque a cada rato te pedira usuario y contraesna y no podras anadir nada a tu repositorio y aunque coloque bien sigue bloqueado

Cuando lo clonas con https te sigue pediendo a cada ratoo usuario y contrasena

###TRUCO

Si me creo un repositorio como nombre de usuario puede ser usado como portafolio y se anade al perfil como un portafolio
Ahora por 5 puntos del examen debemos crear nuestro portafolio en github

