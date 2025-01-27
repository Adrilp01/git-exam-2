- ¿Qué comando utilizaste en el paso 11? ¿Por qué?
Empleé el comando git reset --hard HEAD~1. Porque con este cambio eliminamos el último commit y no dejamos nada en el working copy. Si hubiese empleado git reset HEAD~1 habría eliminado el último commit pero mis modificaciones hubieran quedado en el working copy.

- ¿Qué comando o comandos utilizaste en el paso 12? ¿Por qué?
Utilicé git reflog para ver el identificador de mi último commit, tras esto lo copié y empleé el código git reset --hard “código” para que me llevase de vuelta a ese commit.

- El merge del paso 13, ¿Causó algún conflicto? ¿Por qué?
Me dio que ya estaba actualizada. Esto sucede porque al hacer el merge no hemos introducido nuevos cambios, es decir los commits que estaban en main ya estaban en styled

- El merge del paso 19, ¿Causó algún conflicto? ¿Por qué?
CONFLICT (content): Merge conflict in git-nuestro.md Automatic merge failed; fix conflicts and then commit the result.
Ocurre ese conflict. El conflicto se debe a que el archivo que estamos editando es diferente en cada rama y al hacer el merge git no sabe cual priorizar.

- El merge del paso 21, ¿Causó algún conflicto? ¿Por qué?
No, se debe a que no se había hecho modificado ningún archivo en main que pudiera generar un conflicto con styled. Git ha movido el puntero más hacia delante sin problemas.

- ¿Qué comando o comandos utilizaste en el paso 25?
Utilicé git log –graph, pero podría haber empleado otros como git log –pretty=oneline o git log – graph –decorate –pretty=oneline

- El merge del paso 26, ¿Podría ser fast forward? ¿Por qué?
Creo que no podría serlo ya que se ha realizado un commit dentro de title, por lo que si quisiéramos que git lo absorbiera tendríamos un conflicto al haber dos versiones del mismo archivo, en este caso igual que antes tendriamos que seleccionar manualmente con cual queremos quedarnos.

- ¿Qué comando o comandos utilizaste en el paso 27?
Git reset HEAD~1, para no eliminar el working copy.

- ¿Qué comando o comandos utilizaste en el paso 28?
Git restore git-nuestro.md. Estaba en el working copy y al realizar un git status se decía que con dicho comando se procedería al descarte de los cambios

- ¿Qué comando o comandos utilizaste en el paso 29?
Use git branch -d title pero no era válido usarlo debido a que title no estaba mergeado, entonces use git branch -D title

- ¿Qué comando o comandos utilizaste en el paso 30?
Git reset --hard “código_posicion”, volvi hacia atrás con ese comando.

- ¿Qué comando o comandos usaste en el paso 32?
Use git reflog para ver el código de la posición del commit inicial y después use it reset --hard “código_posicion”.

- ¿Qué comando o comandos usaste en el punto 33?
Use git reflog para ver el código de la posición del commit inicial y después use git reset --hard “código_posicion”.
