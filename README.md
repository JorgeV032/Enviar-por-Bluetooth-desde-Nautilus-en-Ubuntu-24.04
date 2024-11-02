# Enviar-por-Bluetooth-desde-Nautilus-en-Ubuntu-24.04
Añade la opción de Enviar por Bluetooth desde Nautilus en Ubuntu 24.04



### Paso 1: Instala la aplicación de gestión de bluetooth Blueman.
  ```
  sudo apt install blueman
  ```



### Paso 2: Navega hasta la carpeta de scripts de Nautilus.
  ```
  cd ~/.local/share/nautilus/scripts
  ```



### Paso 3: Copia en esta ruta el fichero "Enviar por Bluetooth", que puedes descargar de este repositorio, o bien créalo.
  ```
  nano Enviar por Bluetooth
  ```



### Paso 4: Si lo creaste en vez de copiarlo, pon el siguiente código en él.
  ```
  #!/bin/bash
  for filepath in "$@"; do
      blueman-sendto "$filepath"
  done
  ```



### Paso 5: Reinicia Nautilus.
  ```
  nautilus -q
  ```
