#Respuestas al Ejercicio 1

##P1: comando utilizado en el paso 11. ¿Porqué?
- `git reset --hard HEAD~1``
- *git reset HEAD~1* deshace el último commit pero para modificar el working copy utilizo *--hard*

##P2: comando/s utilizados en el paso 12. ¿Por qué?

-  `git reflog`, copiar identificador del commit donde añadiamos itálicas: *5a66eaa*
-  `git reset --hard 5a66eaa`
	
-  Para moverme a un commit al que no tengo acceso desde mi posición actual, HEAD, tengo que buscar el identificador del commit al que quiero moverme en el reflog. Búsco el commit con el último mensaje que he escrito. Utilizo el hash del commit junto al comando *git reset* para desplazar la rama y head a ese commit y el modificador *-- hard* para restablecer los cambios en el working copy

##P3: merge paso 13. ¿Conflicto? ¿Por qué?

- No porque **styled** ya tenía acceso a  todo el contenido de **master** y no supone ningún cambio.

##P4: merge paso 19. ¿Conflicto? ¿Por qué? 

- Si se causa un conflicto porque el commit al que apunta **styled** contiene la versión con itálicas y la de **htmlify** la versión en las que en las mismas líneas hay etiquetas html. Las mismas líneas tienen contenido diferente por lo que hay conflicto.

##P5: merge paso 21. ¿Conflicto? ¿Por qué?

- No hay conflicto porque sólo es necesario hacer un merge fast-forward moviendo **master** a donde está **styled** que tenia acceso a todos los commits

##P6: comando/s paso 25

- Uso `git graph` porque tengo un **alias** con ese nombre para el comando: `git log --graph --decorate --pretty=online`. 

##P7: merge paso 26. ¿fast forward? ¿Por qué?

- El merge si podría haber sido fast-forward porque sólo era necesario apuntar **master** al commit al que apunta **title** y no se perdería información ya que desde **title** ya se tenía acceso a todos los commits.

##P8: comando/s paso 27

- `git reset HEAD~1`

##P9: comando/s paso 28

- `git checkout -- git-nuestro.md`

##P10: comando/s paso 29

- `git branch -D title`
- Es necesario usar la **D** mayúscula porque el commit al que apunta **title** se queda sin acceso desde donde estamos en ese momento.

##P11: comando/s paso 30

- `git reflog` y copiar el hash del comit del merge: *ad3e7b1*
- `git reset ad3e7b1` para llevar la rama master a ese commit.
	 
##P12: comando/s paso 32

- `git reflog` y copiar el hash del commit inicial: *5aa4f6f*
- `git reset --hard 5aa4f6f` para restablecer el contenido del working copy

##P13: comando/s paso 33
 
 - `git reflog` y copiar el hash del commit del merge con titulo y master: *c1df59f*
 - `git reset --hard c1df59f` para restablecer el contenido del working copy

