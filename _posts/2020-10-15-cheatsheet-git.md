---
layout: post
title: Cheatsheet de comandos Git
categories: cheatsheet
permalink: /cheatsheet-git/
published: true
---
### Eliminar commits de rama local luego de push hacia rama remota

*Esto no se debe hacer si los usuarios ya se han descargado copias de los cambios pusheados.*

- Hard reset hacia un commit específico

    `git reset --hard 0a2fffb`
  
- Push forzado a la rama remota

    `git push -f origin master`
  
### Configurar salto de líneas en Windows para interoperabilidad

- Editar variable global

    `git config --global core.autocrlf true`
  
- Luego del cambio, normalizar los archivos

    * Guardar los cambios locales para prevenir pérdida de información

        `git add . -u`
        
        `git commit -m "Guardando archivos antes de editar saltos de linea"`
        
    * Agregar todos los archivos modificados y normalizarlos 
    
        `git add --renormalize .`
        
    * Guardar los cambios de la normalización  
        
        `git commit -m "Guardando archivos con saltos de linea editados"`

### Actualizar el archivo `.gitignore`

- Borrar de la cache todos los archivos

    `git rm -r --cached .`
  
- Volver a agregar los archivos tomando en cuenta las nuevas reglas del `.gitignore` 

    `git add .`

- Guardar cambios 

    `git commit -m ".gitignore actualizado"`