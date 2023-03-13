# git-tutorial
Un tutorial práctico de Git y GitHub!
## Conceptos básicos de Git:
### ¿Qué es Git?
Git es un sistema descentralizado de control de versiones de código abierto y grtuito.  
Veamos qué significa todo esto.  
Git es un **sistema**. Esto significa que Git posee un conjunto de funcionalidades que 
permiten un flujo de trabajo organizado para un fin específico.  
Git es **descentralizado**. Esto significa que Git permite el trabajo en conjunto sin la 
necesidad de mantener un único registro centralizado.  
Git permite **controlar versiones** de nuestro código/proyecto. Esto quiere decir que 
Git "mira" nuestro código y registra los cambios que ocurren en éste de forma eficiente.  
### ¿Qué es GitHub?
GitHub es un servicio en la nube para desarrolladores para almacenar y compartir código 
gestionado con Git.
### Repositorios
Los repositorios de código, llamados también repos, son carpetas donde se almacenan 
código fuente y otra carpeta con un directorio oculto creado por Git para mantener un 
control sobre los cambios se vayan realizando sobre el mismo.
### Commits
Son los cambios que se van registrando en el código fuente. Consisten en un mensaje corto 
que describe el o los cambios realizados junto con su correspondiente registro.
### Staging
Es un mecanismo usado para evitar que el código ya listo para commit en un archivo se 
vea afectado por error. Está pensado cuando un cambio requiere ser aplicado en varios 
archivos.
### Branches
También llamadas ramas. Es un mecanismo que permite trabajar con una copia del proyecto 
original tomando un commit como base. Es un mecanismo particularmente útil para el 
desarrollo, ya que permite la colaboración entre desarrolladores y la protección del 
código que "ya funciona" en una "rama maestra o prinipal" (llamada master o main).
### Merging
Es un mecanismo que analiza las diferencias entre el código de dos ramas y las fusiona en
una sola. Este es el proceso por el cual varios desarrolladores pueden colaborar entre 
sí, cada uno creando ramas sobre las cuales añaden una nueva funcionalidad y luego fusionan 
las ramas con cuidado para implementar las nuevas funciones del software.
## ¿Cómo uso Git y GitHub?
Lo primero es crear una carpeta en la que va a ir el proyecto.  
Lo siguiente es abrir una consola, terminal o línea de comandos y ubicarse en dicha carpeta.  
Ahora simplemente escribimos lo siguiente:
>git init
>
Con esto Git crea un nuevo repositorio con el mismo nombre que nuestra carpeta. Ahora Git
mirará todos los cambios que ocurran dentro de ella.  
Supongamos que iniciamos a escribir código, por ejemplo, una sencilla calculadora en 
Python. Digamos que vamos a hacer primero un programa que lea dos números y los sume:
>def suma():  
	a = 0  
	b = 0  
	while(True):  
		try:  
			a = int(input("Ingrese un nro: "))  
			b = int(input("Ingrese otro nro: "))  
			break  
		except:  
			print("[ERROR] Datos incorrectos.")  
			input("Presione ENTER para continuar...")  
			continue  
	return a + b  
>
Ahora vamos a hacer un commit. Para ello debemos configurar Git como sigue:
>git config --global user.name "Jakku Night"  
git config --global user.email "j97k107u45k117n@gmail.com"
>
En este caso, mi nombre de usuario (user.name) es "Jakku Night", y mi correo electrónico 
(user.email) es "j97k107u45k117n@gmail.com".  
Esto le indica a Git quien "firma" cada commit.  
Para hacer un commit, debemos mover los archivos que ya consideramos listos al staging area 
con el siguiente comando:
>git add calculadora.py
>
En este caso, "calculadora.py" es el nombre de mi archivo a añadir (add) al staging area de 
Git. También podemos pasarle una lista de archivos separados por comas y/o espacios.  
Otra forma es pasándole la opción "-A", que le indica Git que añada al staging area TODOS 
los archivos que hayan sido modificados desde el último commit.  
Ahora bien, ya podemos hacer un commit mediante el siguiente comando:
>git commit -m "Funcion de suma anadida."
>
Recuerda que Git, al funcionar desde la consola, no admite caracteres con acentos o tildes, 
por lo que si no quieres que tu mensaje quede así de feo, te aconsejo escribirlo en inglés.  
Ahora abrimos el navegador web. Vamos a crear una cuenta de GitHub.  
Una vez creada, vamos al apartado de repositorios y vamos a crear un nuevo repositorio.
Una vez creado, vamos a copiar su URL (en mi caso: https://github.com/jakkunight/calc-py).  
Nótese que las URLs siguen la estructura: https://github.com/usuario/repositorio.  
Volviendo a nuestra terminal, escribimios el siguiente comando:
>git remote add origin master https://github.com/jakkunight/calc-py
>
Con esto, ya tenemos asociados nuestro **"repositorio local"** (el que se encuentra en 
nuestro equipo) y el **"repositorio remoto"** (el que se encuentra en los servvidores de 
GitHub).  
Antes de sincronizar los cambios, debemos crear un Personal Access Token en los ajustes de 
nuestra cuenta para poder realizar la sincronización. Esto es así para garantizar la 
seguridad de nuestra cuenta y nuestro código, ya que en caso contrario cualquiera podría 
realizar modificaciones sin autorización y compromeeter el proyecto. Asegúrate de guardar 
bien ese token, ya que lo tendremos que utilizar varias veces al realizar cambios en el 
código.
Ahora sincronizamos los cambios con el siguiente comando:
>git push origin master
>
Git nos pedirá nuestras credenciales de la cuenta de GitHub, es decir, el nombre de usuario 
y el token previamente generado.
una vez ingresados, los cambios se sincronizarán en el repositorio remoto.  
¡Listo! Eso es el uso básico de Git y GitHub.

## Fuentes y referencias:
* [Web oficial de Git](https://git-scm.com)
* [Wikipedia](https://es.wikipedia.org/wiki/Git)
* [GitHub Docs](https://docs.github.com/es/get-started/quickstart/hello-world)

