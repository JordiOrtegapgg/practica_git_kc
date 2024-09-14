# practica_git_kc
practica git and github

- ¿Qué comando utilizaste en el paso 11? ¿Por qué?
git reset --hard HEAD~1
"git reset HEAD~1" me permite deshacer un commit y "--hard" elimina cambios en el working copy.
Se podría haber hecho un git reset HEAD~1 + git restore *, pero como tenía necesidad de seleccionar un archivo se ha obtado por --hard.

- ¿Qué comando o comandos utilizaste en el paso 12? ¿Por qué?
"git reflog" para identificar el hash del commit que deshicimos y una vez identificado "git reset --hard <hash>"

- El merge del paso 13, ¿Causó algún conflicto? ¿Por qué?
"git merge main". No causó conflicto, la rama styled ya contenía los commits de main.

- El merge del paso 19, ¿Causó algún conflicto? ¿Por qué?
"git merge htmlify".
Auto-merging git-nuestro.md
CONFLICT (content): Merge conflict in git-nuestro.md
Automatic merge failed; fix conflicts and then commit the result.

Cuando Styled quiere absorver la rama htmlify el archivo git-nuestro.md tenía distinto contenido. Conflicto:

$ cat git-nuestro.md
<<<<<<< HEAD
*Git* nuestro que estás en los repos
Comprimidos sean tus *commits*
Venga a nosotros tu *log*
En el local como en el *remote*
Danos hoy nuestro *pull* de cada día
Perdona nuestros *conflictos*
Como también perdonamos los de otros geeks
No nos dejes caer en *detached HEAD*
y líbranos de *SVN*
`git commit --amend`
=======
<p><em>Git</em> nuestro que estas en los repos<br />
Comprimidos sean tus <em>commits</em><br />
Venga a nosotros tu <em>log</em><br />
En el local como en el <em>remote</em><br />
Danos hoy nuestro <em>pull</em> de cada día<br />
Perdona nuestros <em>conflictos</em><br />
Como también perdonamos los de otros geeks<br />
No nos dejes caer en <em>detached HEAD</em><br />
y líbranos de <em>SVN</em><br />
<code>git commit --amend</code></p>
>>>>>>> htmlify

- El merge del paso 21, ¿Causó algún conflicto? ¿Por qué?
No, porque ambas ramas tenían el mismo contenido en git-nuestro.md, la única diferencia es que una contenía palabras en cursiva (pero esta diferencia no genera conflicto)

- ¿Qué comando o comandos utilizaste en el paso 25?
"git log --graph" y "gitk -all"

- El merge del paso 26, ¿Podría ser fast forward? ¿Por qué?
"git merge --no-ff title"
Sí, huebira podido ser fast forward porque las 2 ramas que participan del merge estaban alineadas (sin commits "ramificaciones" entre ellos...)

- ¿Qué comando o comandos utilizaste en el paso 27?
"git reset HEAD~1" (sin perder los cambios en el working copy)

- ¿Qué comando o comandos utilizaste en el paso 28?
"git restore git-nuestro.md"

- ¿Qué comando o comandos utilizaste en el paso 29?
"git branch -d title"
"git branch -D title"

- ¿Qué comando o comandos utilizaste en el paso 30?
"git reflog". Identificamos b25167b HEAD@{1}: merge title: Merge made by the 'ort' strategy.
"git merge b25167b"

- ¿Qué comando o comandos usaste en el paso 32?
"git checkout <hash>"

- ¿Qué comando o comandos usaste en el punto 33?
"git checkout <hash>"
