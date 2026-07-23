# Desafío
## Bandit Level 0
### Level Goal
The goal of this level is for you to log into the game using SSH. The host to which you need to connect is bandit.labs.overthewire.org, on port 2220. The username is bandit0 and the password is bandit0. Once logged in, go to the Level 1 page to find out how to beat Level 1.

#### Commands you may need to solve this level
```
ssh
```

Helpful Reading Material
Secure Shell (SSH) on Wikipedia
How to use SSH with a non-standard port on It's FOSS
How to use SSH with ssh-keys on wikiHow

## Bandit Level 0 → Level 1
### Level Goal
The password for the next level is stored in a file called readme located in the home directory. Use this password to log into bandit1 using SSH. Whenever you find a password for a level, use SSH (on port 2220) to log into that level and continue the game.

#### Commands you may need to solve this level
```
ls , cd , cat , file , du , find
```

TIP: Create a file for notes and passwords on your local machine!

Passwords for levels are not saved automatically. If you do not save them yourself, you will need to start over from bandit0.

Passwords also occasionally change. It is recommended to take notes on how to solve each challenge. As levels get more challenging, detailed notes are useful to return to where you left off, reference for later problems, or help others after you've completed the challenge.

# Documentación

Elegí documentar tanto el nivel 0 como el 0 → 1, ya que ambos se resuelven en la misma máquina virtual.

## bandit0

### Experiencia:
Comencé usando MobaXterm, una herramienta para trabajo remoto que ofrece múltiples funciones pensadas para programadores, administradores web, administradores de TI y, en general, para cualquier persona que necesite gestionar tareas remotas de forma sencilla en Windows. Facilita enormemente la conexión SSH, ya que cuenta con una herramienta dedicada que solo pide la información básica: puerto, dominio o IP, usuario y contraseña.

Sin embargo, como mi objetivo es entrenar Linux para ciberseguridad, decidí trabajar todo desde la terminal, ya que es más rápido y no siempre se cuenta con una interfaz gráfica que muestre el contenido o las opciones disponibles con solo un clic.

### Procedimiento:
Se utilizó el siguiente comando para conectarse de forma remota a la VM:

```bash
ssh -p 2220 bandit0@bandit.labs.overthewire.org
```

| Parte del comando | Significado |
|---|---|
| `ssh` | Inicia una conexión remota segura que permite acceder y administrar un equipo de forma cifrada |
| `-p` | Indica el puerto al que SSH debe conectarse; si no se especifica, se utiliza el 22 por defecto |
| `2220` | Valor del parámetro `-p`; indica que la conexión se realizará a través del puerto 2220 |
| `bandit0` | Nombre de usuario con el que se iniciará sesión en el servidor remoto |
| `@` | Separador que une el nombre de usuario con el servidor al que se desea conectar |
| `bandit.labs.overthewire.org` | Nombre del dominio (hostname) del servidor remoto |

Tras ingresar el comando, se solicita la contraseña, que es `bandit0`, proporcionada por el propio nivel.

Con esto se da por terminado el nivel 0, ya que únicamente se pedía conectarse por SSH a la máquina virtual.
![Acceso bandit0](../img/Level%200/AccederBandit0.png)


## bandit0 ➸ bandit1

### Experiencia:
Como ya sabía manejar lo básico —listar el contenido de un directorio, crear carpetas, moverme entre directorios, crear archivos, cambiar permisos y algunas rutas comunes, como la configuración de red o el despliegue de un servicio web como Nginx—, no fue complicado encontrar el archivo `readme` e imprimir su contenido.

### Procedimiento:
Una vez dentro de la máquina de bandit0, bastó con ejecutar un `ls`, ya que al iniciar sesión se accede directamente al home del usuario (también se puede llegar ahí con `cd ~`). Luego, con `cat readme` se muestra el contenido del archivo, que contiene la contraseña necesaria para acceder a la siguiente VM.

![Contraseña bandit1](../img/Level%200/ContraseñaBandit1.png)