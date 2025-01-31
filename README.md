<p align="center">
  <picture>
    <source media="(max-width: 600px)" srcset="git.png" />
    <img src="git.png" alt="Descripción" width="300">
  </picture>
</p>

<h1 align="center">Guía Básica de configuración de Git en Español</h1>

## Configurar Git
1. Descargar Git https://git-scm.com/downloads 
2. En _*Consola de comandos*_ o _*Git Bash*_ para verificar que git esta instalado escriba:
   
```shell
Git --version
```
                 
> Si todo esta bien deberia de ver algo parecido a esto:

```
git version 2.7.4
```

3. Para configurar Git debes definir algunas variables globales: `user name` y `user email`. Ambas son necesarias para realizar confirmaciones.
  
4. Establezca su nombre _en la consola_ de comandos. Reemplácelo <USER_NAME> con el nobre de usuario que desee utilizar.
   
```
git config --global user.name "<USER_NAME>"
```

5. Ahora ingresamos el siguiente comando para crear una `user.email` y reemplazamos `<USER_EMAL> con nuestra dirección de correo electrónico:
   
```
git config --global user.email "<USER_EMAIL>"
```

6. A continuación ejecutamos el comando para verivicar que todos los cambios funcionaron:
   
```
git config --list
```

> Si todo va bien nos debe poner algo como esto
```
user.name=Nombre usuario
user.email=correo@email.com
```

![bannergit](https://github.com/user-attachments/assets/7982921c-92bb-49ab-900f-320139beafcc)

## Configura tu repositorio Git

Vamos a crear una carpeta que servirá como nuestro _***árbol de trabajo***_ y se lo comunicaremos a Git para que lleve un seguimiento de los cambios. Para ello crearemos un repositorio de git en esa carpeta.<br>

+ Vamos a crear una carpeta por ejemplo en: `Documents/Proyectosgit/Configurar_git`<br>

+ La carpeta `Configurar_git` ubicada dentro de documentos/ProyectosGit es donde vamos a almacenar todos los archivos relacionados con el proyecto.<br>
+ Usted puede ubicarla donde lo desee, esto es solo un archivo de pruebas, aunque es recomendable hacer una `carpeta de proyectos` y en su interior una carpeta individual para cada proyecto, para mantener el orden y tenga una ruta clara en sus trabajos.

📖 Abrimos la consola de comandos Git Bash
> Buscamos la carpeta que hemos creado con `cd` y la ruta de nuestra carpeta.
> 
> E introducimos la secuencia `git init --initial-branch=main`<br>

![config](https://github.com/user-attachments/assets/61214ff9-b0b0-4bc3-a01b-0da493a2f1f7)

Seguidamente usaremos el siguiente comando para ver que estamos en la rama `main`
```
git status
```
<br><br>

## Creación de SSH (Opcional)
+ ¿Qué es SSH?<br>

_***SSH Secure Shell***_ es un protocolo de comunicación segura, utilizado para acceder y administrar dispositivos de forma remota a través de una red no segura (como Internet). Es muy utilizado en administración de servidores, transferencia de archivos y para ejecutar comandos en máquinas remotas de manera cifrada.¡Y como no en Github! :octocat: <br><br>

Ventajas
+ 🔐 Seguridad: La clave SSH proporciona una autenticación más segura y protege los datos con cifrado.
+ :accessibility: Comodidad: Te ahorra tener que ingresar tu nombre de usuario y contraseña cada vez.
+ 🛂 Control: Puedes gestionar claves SSH específicas por dispositivo o uso.
+ ↪️ Automatización: Permite que herramientas de integración continua y scripts interactúen sin comprometer la seguridad.
+ ⏩ Rapidez: Las conexiones SSH suelen ser más rápidas y confiables

#### 1.Genera una clave SSH con el siguiente comando:

```
ssh-keygen -t rsa -b 4096 -C "tu_correo@ejemplo.com"
```
> Enter passphrase (empty for no passphrase):<br>
Enter same passphrase again:<br>
Si dejas el campo vacío, no se agregará ninguna passphrase, y la clave se generará sin protección adicional. Si decides agregarla, cada vez que uses la clave SSH, se te pedirá la passphrase.
#### 2.Agrega la clave SSH al agente de autenticación

```
eval "$(ssh-agent -s)"
ssh-add ~/.ssh/id_rsa
````

#### 3.Agregar la clave SSH a tu cuenta de GitHub:

Copia la clave pública con el siguiente comando:

```
cat ~/.ssh/id_rsa.pub
```

Esto te mostrará la clave pública en la terminal. _***COPIA TODO EL CONTENIDO***_
+ Ve a GitHub SSH settings.
+ Haz clic en New SSH Key.
+ Pega la clave que copiaste en el campo correspondiente y ponle un título para identificarla.( POR EJEMPLO : MI PC WINDOWS )
+ Haz clic en Add SSH Key.
  
<br>

![ssh](https://github.com/user-attachments/assets/964b602e-e121-42e3-8194-dd774e48b334)

![banner2](https://github.com/user-attachments/assets/86c9ac39-54bc-43f8-9456-02cc020d8c54)

