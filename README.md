# Configurar Git
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
