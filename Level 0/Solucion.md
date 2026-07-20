# Desafió
## Bandit Level 0
### Level Goal
The goal of this level is for you to log into the game using SSH. The host to which you need to connect is bandit.labs.overthewire.org, on port 2220. The username is bandit0 and the password is bandit0. Once logged in, go to the Level 1 page to find out how to beat Level 1.

#### Commands you may need to solve this level

<p style="color: #2563EB;">ssh</p> 

Helpful Reading Material
Secure Shell (SSH) on Wikipedia
How to use SSH with a non-standard port on It’s FOSS
How to use SSH with ssh-keys on wikiHow

## Bandit Level 0 → Level 1
### Level Goal
The password for the next level is stored in a file called readme located in the home directory. Use this password to log into bandit1 using SSH. Whenever you find a password for a level, use SSH (on port 2220) to log into that level and continue the game.

#### Commands you may need to solve this level
ls , cd , cat , file , du , find

TIP: Create a file for notes and passwords on your local machine!

Passwords for levels are not saved automatically. If you do not save them yourself, you will need to start over from bandit0.

Passwords also occasionally change. It is recommended to take notes on how to solve each challenge. As levels get more challenging, detailed notes are useful to return to where you left off, reference for later problems, or help others after you’ve completed the challenge.

# Documentación
Elegí documentar tanto el nivel 0 como el 0 -> 1 debido a que se trabaja en la misma maquina virtual.
### bandit0
Experiencia:
- Comencé a utilizar el MobaXterm que es una caja de herramientas para trabajo remoto debido a que ofrece una gran cantidad de funciones diseñadas para programadores, administradores web (webmasters), administradores de Ti y en general para cualquier persona que necesite gestionar tareas remotas de una manera sencilla en windows esta facilita enormemente el escribir el comando completo, debido a que tiene una herramienta explícitamente de ssh el cual solo te pide la info básica de que puerto, dominio o ip, usuario y contraseña

- Como mi proposito es entrenar Linux para ciberseguridad hare todo por la terminal debido a que es mas rápido y no siempre se tendrá una linda interfaz para visualizar el contenido o tener todas las opciones a la mano con solo usar el clic

Procedimiento:
Se utilizo el siguiente comando para conectarse via remota hacia la vm el cual es: ​``` ssh -p 2220 bandit0@bandit.labs.overthewire.org ```  luego de ingresar ese comando te solicitara la contraseña la cual es bandit0 que es bandit0 la cual viene proporcionada en la misma indicación del desafió
- Se utiliza el comando ssh
- Modificador -p para especificar el puerto que es el 2220
- nombre de usuario que es bandit0
