# Desafió
## Bandit Level 0
### Level Goal
The goal of this level is for you to log into the game using SSH. The host to which you need to connect is bandit.labs.overthewire.org, on port 2220. The username is bandit0 and the password is bandit0. Once logged in, go to the Level 1 page to find out how to beat Level 1.

#### Commands you may need to solve this level
<div style="text-align:center; margin:1em 0;"><p style="color: #eb2525;">ssh</p> </div>
 

Helpful Reading Material
Secure Shell (SSH) on Wikipedia
How to use SSH with a non-standard port on It’s FOSS
How to use SSH with ssh-keys on wikiHow

## Bandit Level 0 → Level 1
### Level Goal
The password for the next level is stored in a file called readme located in the home directory. Use this password to log into bandit1 using SSH. Whenever you find a password for a level, use SSH (on port 2220) to log into that level and continue the game.

#### Commands you may need to solve this level
<div style="text-align:center; margin:1em 0;"><p style="color: #eb2525;">ls , cd , cat , file , du , find</p></div>


TIP: Create a file for notes and passwords on your local machine!

Passwords for levels are not saved automatically. If you do not save them yourself, you will need to start over from bandit0.

Passwords also occasionally change. It is recommended to take notes on how to solve each challenge. As levels get more challenging, detailed notes are useful to return to where you left off, reference for later problems, or help others after you’ve completed the challenge.

# Documentación
Elegí documentar tanto el nivel 0 como el 0 -> 1 debido a que se trabaja en la misma maquina virtual.
## bandit0
### Experiencia:
- Comencé a utilizar el MobaXterm que es una caja de herramientas para trabajo remoto debido a que ofrece una gran cantidad de funciones diseñadas para programadores, administradores web (webmasters), administradores de Ti y en general para cualquier persona que necesite gestionar tareas remotas de una manera sencilla en windows esta facilita enormemente el escribir el comando completo, debido a que tiene una herramienta explícitamente de ssh el cual solo te pide la info básica de que puerto, dominio o ip, usuario y contraseña

- Como mi propósito es entrenar Linux para ciberseguridad hare todo por la terminal debido a que es mas rápido y no siempre se tendrá una linda interfaz para visualizar el contenido o tener todas las opciones a la mano con solo usar el clic

### Procedimiento:
Se utilizo el siguiente comando para conectarse via remota hacia la vm el cual es: Se utilizó el siguiente comando para conectarse vía remota hacia la VM:

<div style="text-align:center; margin:1em 0;">
    <code>
        <span style="color:#2563EB;">ssh</span>
        <span style="color:#F59E0B;">-p</span>
        <span style="color:#22C55E;">2220</span>
        <span style="color:#A855F7;">bandit0</span><span style="color:#6B7280;">@</span><span style="color:#06B6D4;">bandit.labs.overthewire.org</span>
    </code>
</div>

- <span style="color:#2563EB;">ssh</span>: Inicia una conexión remota segura y nos permite acceder y administrar un equipo remoto de forma cifrada.
- <span style="color:#F59E0B;">-p</span>: Indica el puerto al que el SSH debe conectarse, si este no es especificado se utilizara el 22 que es el que esta por defecto.
- <span style="color:#22C55E;">2220</span>: Valor del parámetro -p y este indica que la conexión se realizara a traves del puerto 2220.
- <span style="color:#A855F7;">bandit0</span>: Nombre de Usuario con el que se iniciara sesión en el servidor remoto.
- <span style="color:#6B7280;">@</span>: Separador que une el nombre del usuario con el servidor a que se desea conectar.
- <span style="color:#06B6D4;">bandit.labs.overthewire.org</span> nombre del dominio (hostname) del servidor remoto.

luego de ingresar el comando se solicitara que se ingrese la contraseña que es bandit0 dada por el mismo nivel

Con esto terminamos el nivel 0, ya que solamente se indica que entremos por ssh a la maquina virtual

## bandit0 ➸ bandit1
### Experiencia:
- Debido a que ya sabia hacer lo básico como listar el contenido de un directorio, crear carpetas, moverme entre directorios, crear archivos, cambiar permisos, algunas de las rutas básicas como donde esta la configuración de red,para el despliegue de un servicio web como Nginx, etc, no fue complicado el encontrar el archivo readme e imprimir su contenido


### Procedimiento:
- Una vez estando dentro de la maquina de bandit0 simplemente fue hacer un ls ya que al ingresar a un vm me mando directamente al home del usuario o bien se puede ir a esa ruta solamente con un cd 
