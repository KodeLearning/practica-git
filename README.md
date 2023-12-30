# Práctica git
Se deberá crear un repositorio y realizar una serie de operaciones **desde la consola de
comandos** sobre el mismo para posteriormente subir el repositorio a Github.

Se deberá entregar a través del formulario de prácticas indicando la URL del repositorio. En el
repositorio, deberá existir un archivo readme.md con las respuestas a las siguientes preguntas:

### ¿Qué comando utilizaste en el paso 11? ¿Por qué?
`git reset --hard HEAD~1` porque queremos volver al commit anterior sin mantener los cambios de ese commit.
`git reset` se utiliza para moverse entre commits, `--hard` se ocupa de eliminar los cambios de tu area de trabajo y actualizarlo al commit al que te mueves.
`HEAD~1` mueve 'HEAD' un commit hacia atrás haciendo que nuestra area de trabajo regrese 1 commit hacia atrás recuperando los cambios de ese commit.
Repito el comando `git reset --hard HEAD~1` porque el primero no devolvía los cambios que debía. ¿Creo que haber hecho el pull lo jodió?
###¿Qué comando o comandos utilizaste en el paso 12? ¿Por qué?
Utilizo el comando `git reflog` para ver el historial de referencias a los otros commits y uso `git reset --hard ` utilizando el hash del commit que me dan para volver a él.

### El merge del paso 13, ¿Causó algún conflicto? ¿Por qué?
Me da un conflicto porque la rama que estoy absorbiendo (main) contiene un texto diferente a las modificaciones hechas en 'styled' por lo que debemos elegir cual es las dos modificaciones queremos mantener o si queremos fusionarlas para mantener las dos.

### El merge del paso 19, ¿Causó algún conflicto? ¿Por qué?
Sí, el mismo caso que en el merge anterior. La rama 'styled' contiene un texto modificado de forma diferente al que tenemos en 'htmlify', por lo que nos obliga a elegir entre una de las dos versiones antes de completar el merge.

### El merge del paso 21, ¿Causó algún conflicto? ¿Por qué?
Sorprendentemente no.

### ¿Qué comando o comandos utilizaste en el paso 25?
`git log --graph`
### El merge del paso 26, ¿Podría ser fast forward? ¿Por qué?
Sí porque en la rama main no se ha trabajado, no hay cambios ni ningún commit por lo que se puede fusionar title a main sin necesidad de hacer un merge normal
### ¿Qué comando o comandos utilizaste en el paso 27?
Utilizo el `git reflog` para ver el hash de referencia al commit anterior al merge y luego un `git reset` con ese hash para volver manteniendo los cambios actuales.
### ¿Qué comando o comandos utilizaste en el paso 28?
Utilizo `git restore` con el nombre del archivo para recuperar el código original.
### ¿Qué comando o comandos utilizaste en el paso 29?
Utilizo `git branch -d title` y `git push --delete origin title` para eliminar la rama tanto de local como del remoto
### ¿Qué comando o comandos utilizaste en el paso 30?
Vuelvo a utilizar `git reflog` para ver el hash del merge y utilizo `git reset --hard` para volver al merge que había deshecho recuperando sus cambios
### ¿Qué comando o comandos usaste en el paso 32?
Utilizo `git log` para encontrar el primer commit y utilizo su hash en `git reset --hard` para recuperarlo por completo.
### ¿Qué comando o comandos usaste en el punto 33?
Utilizo `git reflog` para encontrar commits superiores y utilizo su hash con `git reset --hard` para recuperar los cambios que había deshecho
