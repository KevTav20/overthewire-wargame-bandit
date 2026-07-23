# Desafío

# Bandit Level 0

## Level Goal

The goal of this level is for you to log into the game using SSH. The host to which you need to connect is **bandit.labs.overthewire.org**, on port **2220**. The username is **bandit0** and the password is **bandit0**. Once logged in, go to the Level 1 page to find out how to beat Level 1.

### Commands you may need to solve this level

- `ssh`

### Helpful Reading Material

- Secure Shell (SSH) on Wikipedia
- How to use SSH with a non-standard port on It's FOSS
- How to use SSH with SSH-keys on wikiHow

---

# Bandit Level 0 → Level 1

## Level Goal

The password for the next level is stored in a file called `readme` located in the home directory. Use this password to log into **bandit1** using SSH. Whenever you find a password for a level, use SSH (on port **2220**) to log into that level and continue the game.

### Commands you may need to solve this level

- `ls`
- `cd`
- `cat`
- `file`
- `du`
- `find`

> **TIP:** Create a file for notes and passwords on your local machine.
>
> Passwords for levels are not saved automatically. If you do not save them yourself, you will need to start over from bandit0.
>
> Passwords also occasionally change. It is recommended to take notes on how to solve each challenge. As levels get more challenging, detailed notes are useful to return to where you left off, reference for later problems, or help others after you've completed the challenge.

---

# Documentación

Los niveles **Bandit 0** y **Bandit 0 → 1** se documentan en conjunto, ya que ambos se realizan dentro de la misma máquina virtual.

---

# Bandit Level 0

## Descripción

El objetivo de este nivel consiste en establecer una conexión remota mediante el protocolo **SSH** utilizando las credenciales proporcionadas por el desafío.

Aunque herramientas como **MobaXterm** facilitan este proceso mediante una interfaz gráfica, toda la documentación fue realizada desde la terminal con el propósito de fortalecer el manejo de comandos de Linux y familiarizarse con el entorno utilizado habitualmente en ciberseguridad.

## Procedimiento

Para conectarse a la máquina virtual se ejecutó el siguiente comando:

```bash
ssh -p 2220 bandit0@bandit.labs.overthewire.org
```

### Desglose del comando

| Parte del comando | Significado |
|-------------------|-------------|
| `ssh` | Inicia una conexión remota segura utilizando el protocolo **Secure Shell (SSH)**. |
| `-p` | Especifica el puerto al que se realizará la conexión. Si se omite, SSH utiliza el puerto **22** por defecto. |
| `2220` | Puerto configurado por el servidor para este desafío. |
| `bandit0` | Usuario con el que se iniciará sesión en el servidor remoto. |
| `@` | Separador entre el nombre del usuario y el servidor remoto. |
| `bandit.labs.overthewire.org` | Nombre del dominio (hostname) del servidor donde se aloja el laboratorio Bandit. |

Una vez ejecutado el comando, el servidor solicita la contraseña correspondiente al usuario **bandit0**, la cual es proporcionada por el propio desafío.

Al autenticarse correctamente se completa el nivel.

## Comandos aprendidos

| Comando | Descripción |
|----------|-------------|
| `ssh` | Permite establecer una conexión remota segura con otro equipo mediante el protocolo SSH. |

## Evidencia

![Acceso bandit0](../img/Level%200/AccederBandit0.png)

---

# Bandit Level 0 → Level 1

## Descripción

El objetivo de este nivel consiste en localizar el archivo `readme`, ubicado dentro del directorio personal del usuario, y obtener la contraseña necesaria para acceder al siguiente nivel.

## Procedimiento

Al iniciar sesión mediante SSH, el usuario es ubicado automáticamente en su directorio personal (**Home**). No es necesario desplazarse hasta él, aunque también es posible hacerlo utilizando:

```bash
cd ~
```

Para comprobar el contenido del directorio se ejecutó:

```bash
ls
```

### Desglose del comando

| Parte del comando | Significado |
|-------------------|-------------|
| `ls` | Lista los archivos y directorios contenidos en el directorio actual. |

Como resultado se identificó el archivo `readme`.

Posteriormente se ejecutó:

```bash
cat readme
```

### Desglose del comando

| Parte del comando | Significado |
|-------------------|-------------|
| `cat` | Muestra el contenido de uno o varios archivos de texto en la terminal. |
| `readme` | Archivo que contiene la contraseña necesaria para acceder al siguiente nivel. |

Tras ejecutar el comando, se obtuvo la contraseña correspondiente al usuario **bandit1**, la cual será utilizada para autenticarse en el siguiente desafío.

## Comandos aprendidos

| Comando | Descripción |
|----------|-------------|
| `ls` | Lista el contenido del directorio actual. |
| `cd` | Permite cambiar entre directorios del sistema de archivos. |
| `cat` | Muestra el contenido de un archivo de texto en la terminal. |

## Evidencia

![Contraseña bandit1](../img/Level%200/ContraseñaBandit1.png)