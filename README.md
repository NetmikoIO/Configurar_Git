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

Vamos a crear una carpeta por ejemplo en: `Documentos/Proyectogit`<br>

La carpeta `Proyectogit` ubicada dentro de documentos es donde vamos a almacenar todos los archivos relacionados con el proyecto.

📖 Abrimos la consola de comandos Git Bash
> Buscamos la carpeta que hemos creado con `cd` y la ruta de nuestra carpeta.<br>




