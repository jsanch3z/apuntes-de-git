# Curso Git desde Cero
Sistema de control de versiones para el mantenimiento eficiente y confiable de archivos.

## Zonas de Git
1. Directorio de trabajo
2. Area de preparacion
3. Directorio Git

## Flujo de trabajo
1. Modificas una serie de archivos en tu directorio de trabajo
2. Preparas los archivos, añadiendolos a tu area de preparacion
3. confirms los cambios, lo que toma los archivos tal y como estan en el area de preparacion y  almancena esa copia instantanea de manera permanenete en tu directorio de Git

## configurando Git por primera vez
```
git config --global user.name "Jhon Doe"
git config --global user.email js.sanch3z@gmail.com
git config --global core.editor subl
git config --list

```

## Configuracion SSH en Windows
Usando Git Bash seguimos los siguientes pasos:

1. Creamos una carpeta llamada `llaves-ssh` en el disco `C` para evitar problemas de rutas.

2. Ejecutamos el comando `ssh-keygen -t rsa -C "js.sanch3z@gmail.com"`.
El correo debe ser el mismo con el que nos registramos en Github para evitar posibles problemas. 
Dejamos el passphrase vacio y damos enter.
Cuando nos pida la ruta escribimos `/c/llaves-ssh/github_rsa`.

3. Iniciamos ssh-agent en background ejecutando el comando `eval "$(ssh-agent -s".

4. Agregamos la llave ssh generada a ssh-agent ejecutando el comando `ssh-add /c/llaves-ssh/github_rsa`.

5. Desde ahora podemos hacer pull y push sin que Github nos este pidiendo los datos de acceso.

