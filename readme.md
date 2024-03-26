<h1>Cheatsheet de Git: Guía Rápida</h1>

<h2>Configuración Inicial</h2>

<pre><code> <!-- Configuración Inicial -->
git config --global user.name "Vicent Muñoz Correcher" <!-- Configura el nombre de usuario -->
git config --global user.email vicent.correcher@gmail.com <!-- Configura el correo electrónico del usuario -->

git config --global color.ui true <!-- Habilita el uso de colores en la interfaz de usuario -->
</code></pre>


<ul>
  <li><strong> git config --global user.name: </strong> Este comando establece el nombre de usuario para tu cuenta de Git.</li>
  <li><strong> git config --global user.email</strong> Este comando establece el correo electrónico asociado con tu cuenta de Git.</li>
  <li><strong> git config --global color.ui true</strong> Este comando activa el uso de colores para una mejor visualización en la interfaz de usuario de Git.</li>
</ul>


<h2>Iniciando y Clonando Repositorios</h2>

<pre><code> <!-- Iniciando y Clonando Repositorios -->
git init <!-- Inicia un nuevo repositorio Git en el directorio actual -->
git clone &lt;url&gt; git-demo <!-- Clona un repositorio remoto en un directorio local llamado 'git-demo' -->
</code></pre>

<ul>
  <li><strong>git init: </strong> Este comando crea un nuevo repositorio Git en el directorio actual.</li>
  <li><strong>git clone &lt;url&gt; nombre:</strong> Este comando clona un repositorio remoto en un directorio local con el nombre especificado.</li>
</ul>


<h2>Realizando Cambios</h2>

<pre><code> <!-- Realizando Cambios -->
git add . <!-- Agrega todos los archivos modificados y eliminados al área de preparación -->
git add &lt;archivo&gt; <!-- Agrega un archivo específico al área de preparación -->
git add --all <!-- Agrega todos los archivos modificados, eliminados y nuevos al área de preparación -->
git add *.txt <!-- Agrega todos los archivos con extensión .txt al área de preparación -->
git add docs/*.txt <!-- Agrega todos los archivos con extensión .txt en el directorio 'docs' al área de preparación -->
git add docs/ <!-- Agrega todos los archivos en el directorio 'docs' al área de preparación -->
</code></pre>

<ul>
  <li><strong>git add .:</strong> Este comando añade todos los cambios realizados en los archivos al área de preparación para el siguiente commit.</li>
  <li><strong>git add &lt;archivo&gt;:</strong> Este comando añade un archivo específico al área de preparación para el siguiente commit.</li>
  <li><strong>git add --all :</strong> Este comando agrega todos los cambios realizados en los archivos al área de preparación, incluyendo los archivos nuevos y los eliminados, para el siguiente commit.</li>
  <li><strong>git add *.txt:</strong> Este comando agrega todos los archivos con la extensión .txt al área de preparación para el siguiente commit.</li>
  <li><strong>git add docs/*.txt:</strong> Este comando agrega todos los archivos con la extensión .txt en el directorio 'docs' al área de preparación para el siguiente commit.</li>
  <li><strong>git add docs/:</strong> Este comando agrega todos los archivos en el directorio 'docs' al área de preparación para el siguiente commit.</li>
</ul>


<h2>Realizando Commits</h2>

<pre><code> <!-- Realizando Commits -->
git commit -m "Texto que identifique por qué se hizo el commit" <!-- Crea un nuevo commit con un mensaje descriptivo -->
git commit -a -m "Texto que identifique por qué se hizo el commit" <!-- Agrega todos los archivos modificados y eliminaidos al área de preparación y crea un nuevo commit con un mensaje -->
git commit -a <!-- Agrega todos los archivos modificados y eliminados al área de preparación y abre el editor de texto para escribir un mensaje de commit -->
git commit --amend -m "Nuevo mensaje para el commit" <!-- Modifica el mensaje del último commit -->
</code></pre>

<ul>
  <li><strong>git commit -m "Texto":</strong> Este comando crea un nuevo commit con los cambios en el área de preparación y un mensaje descriptivo que explica los cambios realizados.</li>
  <li><strong>git commit -a -m "Texto":</strong> Este comando agrega todos los archivos modificados y eliminados al área de preparación, luego crea un nuevo commit con un mensaje descriptivo.</li>
  <li><strong>git commit -a:</strong> Este comando agrega todos los archivos modificados y eliminados al área de preparación y abre el editor de texto para que puedas escribir un mensaje de commit detallado.</li>
  <li><strong>git commit --amend -m "Nuevo texto":</strong> Este comando te permite cambiar el mensaje del último commit realizado.</li>
</ul>

<h2>Subiendo Cambios a Repositorios Remotos</h2>

<pre><code> <!-- Subiendo Cambios a Repositorios Remotos -->
git push origin master <!-- Sube los cambios locales al repositorio remoto en la rama 'master' -->
git push --tags <!-- Sube todas las etiquetas locales al repositorio remoto -->
</code></pre>

<ul>
  <li><strong>git push origin master</strong> Este comando envía los cambios locales al repositorio remoto en la rama 'master'.</li>
  <li><strong>git push --tags:</strong> Este comando envía todas las etiquetas locales al repositorio remoto.</li>
</ul>

<h2>Visualizando Historial y Diferencias</h2>

<pre><code> <!-- Visualizando Historial y Diferencias -->
git log <!-- Muestra el historial de commits -->
git log --oneline --stat <!-- Muestra el historial de commits en una línea y estadísticas de cambios -->
git log --oneline --graph <!-- Muestra el historial de commits en una línea con un gráfico ASCII -->
git diff <!-- Muestra las diferencias entre el directorio de trabajo y el área de preparación -->
git diff --staged <!-- Muestra las diferencias entre el área de preparación y el último commit -->
</code></pre>

<ul>
  <li><strong>git log:</strong> Este comando muestra el historial completo de commits en la rama actual.</li>
  <li><strong>git log --oneline --stat:</strong> Este comando muestra el historial de commits en una línea con estadísticas de los cambios realizados en cada commit.</li>
  <li><strong>git log --oneline --graph:</strong> Este comando muestra el historial de commits en una línea con un gráfico ASCII que representa las ramificaciones del proyecto.</li>
  <li><strong>git diff:</strong> Este comando muestra las diferencias entre los archivos en el directorio de trabajo y los archivos en el área de preparación.</li>
  <li><strong>git diff --staged:</strong> Este comando muestra las diferencias entre los archivos en el área de preparación y el último commit realizado.</li>
</ul>

<h2>Manejando el HEAD y Ramas</h2>

<pre><code> <!-- Manejando el HEAD y Ramas -->
git reset HEAD &lt;archivo&gt; <!-- Quita un archivo del área de preparación -->
git reset --soft HEAD^ <!-- Revierte el último commit manteniendo los cambios en el área de preparación -->
git reset --hard HEAD^ <!-- Revierte el último commit y elimina los cambios realizados -->
git reset --hard HEAD^^ <!-- Revierte los dos últimos commits y elimina los cambios realizados -->
git branch &lt;nameBranch&gt; <!-- Crea una nueva rama con el nombre especificado -->
git branch <!-- Muestra todas las ramas locales -->
git branch -d &lt;nameBranch&gt; <!-- Elimina una rama local -->
git branch -D &lt;nameBranch&gt; <!-- Elimina una rama local incluso si tiene cambios sin fusionar -->
</code></pre>

<ul>
  <li><strong>git reset HEAD &lt;archivo&gt;:</strong> Este comando quita un archivo específico del área de preparación, pero conserva los cambios en el directorio de trabajo.</li>
  <li><strong>git reset --soft HEAD^:</strong> Este comando deshace el último commit pero conserva los cambios realizados en el área de preparación.</li>
  <li><strong>git reset --hard HEAD^:</strong> Este comando deshace el último commit y elimina todos los cambios realizados en el directorio de trabajo.</li>
  <li><strong>git reset --hard HEAD^^:</strong> Este comando deshace los dos últimos commits y elimina todos los cambios realizados en el directorio de trabajo.</li>
  <li><strong>git branch &lt;nameBranch&gt;:</strong> Este comando crea una nueva rama con el nombre especificado.</li>
  <li><strong>git branch :</strong> Este comando muestra todas las ramas locales en el repositorio.</li>
  <li><strong>git branch -d &lt;nameBranch&gt;:</strong> Este comando elimina una rama local del repositorio.</li>
  <li><strong>git branch -D &lt;nameBranch&gt;:</strong> Este comando elimina una rama local del repositorio, incluso si tiene cambios que no han sido fusionados.</li>
</ul>

<h2>Etiquetas (Tags) y Rebase</h2>

<pre><code> <!-- Etiquetas (Tags) y Rebase -->
git tag <!-- Lista todas las etiquetas existentes -->
git tag -a &lt;version&gt; -m "Descripción de la versión" <!-- Crea una nueva etiqueta anotada con un mensaje descriptivo -->
git rebase <!-- Reorganiza el historial de commits para que se basen en la última versión del proyecto -->
git rebase --continue <!-- Continúa con el proceso de rebase después de resolver conflictos -->
git rebase --skip <!-- Omite el commit actual durante el proceso de rebase -->
git rebase --abort <!-- Cancela el proceso de rebase y restaura el estado anterior -->
git rebase &lt;nameBranch&gt; <!-- Realiza un rebase de la rama actual sobre la rama especificada -->
</code></pre>
<ul>
  <li><strong>git tag:</strong> Este comando muestra todas las etiquetas existentes en el repositorio.</li>
  <li><strong>git tag -a &lt;version&gt; -m "Descripción de la versión":</strong> Este comando crea una nueva etiqueta anotada con un mensaje descriptivo para identificar una versión específica del proyecto.</li>
  <li><strong>git rebase:</strong> Este comando reorganiza el historial de commits de la rama actual para que se base en la última versión del proyecto.</li>
  <li><strong>git rebase --continue:</strong> Este comando se utiliza para continuar con el proceso de rebase después de resolver conflictos durante la reorganización del historial de commits.</li>
  <li><strong>git rebase --skip:</strong> Este comando se utiliza para omitir el commit actual durante el proceso de rebase.</li>
  <li><strong>git rebase --abort:</strong> Este comando se utiliza para cancelar el proceso de rebase y restaurar el estado del repositorio al estado anterior al inicio del rebase.</li>
  <li><strong>git rebase &lt;nameBranch&gt;:</strong> Este comando realiza un rebase de la rama actual sobre la rama especificada, reorganizando el historial de commits de la rama actual para que se base en la última versión de la rama especificada.</li>
</ul>

<h2>Otros Comandos Útiles</h2>

<pre><code> <!-- Otros Comandos Útiles -->
git status <!-- Muestra el estado del directorio de trabajo y el área de preparación -->
git checkout -- &lt;file&gt; <!-- Descarta los cambios locales en un archivo específico -->
git checkout -b newlocalbranchname origin/branch-name <!-- Crea una nueva rama local y la rastrea desde la rama remota -->
git pull origin &lt;nameBranch&gt; <!-- Obtiene los cambios de la rama remota y los fusiona con la rama local -->
git checkout &lt;nameBranch/tagname&gt; <!-- Cambia al commit asociado con la rama o etiqueta especificada -->
git merge &lt;nameBranch&gt; <!-- Fusiona los cambios de la rama especificada con la rama actual -->
git fetch <!-- Descarga los cambios del repositorio remoto sin fusionarlos con la rama local -->
git rm &lt;archivo&gt; <!-- Elimina un archivo del repositorio y del sistema de archivos -->
</code></pre>
<ul>
  <li><strong>git status:</strong> Este comando muestra el estado actual de los archivos en el directorio de trabajo y en el área de preparación.</li>
  <li><strong>git checkout -- &lt;file&gt;:</strong> Este comando descarta los cambios locales en un archivo específico y lo restaura al estado en el que se encuentra en el último commit.</li>
  <li><strong>git checkout -b newlocalbranchname origin/branch-name:</strong> Este comando crea una nueva rama local y la configura para rastrear una rama remota específica.</li>
  <li><strong>git pull origin &lt;nameBranch&gt;:</strong> Este comando obtiene los cambios de una rama remota y los fusiona con la rama local actual.</li>
  <li><strong>git checkout &lt;nameBranch/tagname&gt;:</strong> Este comando cambia al commit asociado con la rama o etiqueta especificada.</li>
  <li><strong>git merge &lt;nameBranch&gt;:</strong> Este comando fusiona los cambios de una rama especificada con la rama actual.</li>
  <li><strong>git merge &lt;nameBranch&gt; :</strong> Este comando descarga los cambios del repositorio remoto sin fusionarlos con la rama local actual.</li>
  <li><strong>git rm &lt;archivo&gt;:</strong> Este comando elimina un archivo del repositorio y del sistema de archivos local.</li>
</ul>


<h2>Forks: Trabajar con Repositorios Derivados</h2>

<pre><code> <!-- Forks: Trabajar con Repositorios Derivados -->
git remote add upstream &lt;url&gt; <!-- Agrega un nuevo repositorio remoto como 'upstream' -->
git fetch upstream <!-- Obtiene los cambios del repositorio remoto 'upstream' -->
git merge upstream/master <!-- Fusiona los cambios del repositorio remoto 'upstream' en la rama actual -->
</code></pre>

<ul>
  <li><strong>git remote add upstream &lt;url&gt; ':</strong> Este comando agrega un nuevo repositorio remoto como un alias llamado 'upstream'.</li>
  <li><strong>git fetch upstream:</strong> Este comando obtiene los cambios del repositorio remoto 'upstream' sin fusionarlos con la rama local.</li>
  <li><strong>git merge upstream/master:</strong> Este comando fusiona los cambios del repositorio remoto 'upstream' en la rama actual.</li>
</ul>

</body>
</html>
