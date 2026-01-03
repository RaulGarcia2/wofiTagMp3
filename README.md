# wofiTagMp3
Aplicación en python para etiquetar ficheros mp3 por medio de una interfaz con menu wofi
## Requisitos
Se debe tener instalado:
- Librería *python3-eyed3*
- *wofi*

## Instalación
Copiar el fichero *wofiTagMp3* en _$HOME/.local/bin_ o en otra carpeta dentro de la variable _$PATH_

Asegurarnos que el fichero copiado tiene permisos de ejecución:
```
chmod +x $PATH/.local/bin/wofiTagMp3
```

En el fichero está definida una configuración para que el menú wofi aparezca con un estilo, se deberá cambiar al gusto del usuario.

## Utilización
El script está diseñado para ser utilizado desde el administrador de archivos _yazi_, para ello se introduce una linea en el fichero *$HOME/.config/yazi/yazi.toml*:
```
[opener]
play = [
  .....
	{ run = 'wofiTagMp3 "$@"', orphan = true, desc = "Poner etiquetas mp3 a ficheros de audio", for = "unix" },
  .....
]
```
Si seleccionamos algún fichero tipo mp3, al pulsar "O" nos aparecerá un menú en el que escoguiendo la opción 'Poner etiquetas mp3 a ficheros de audio' se ejecutará la aplicación.
