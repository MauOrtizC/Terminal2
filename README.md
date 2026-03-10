# Practica: Git en Terminal con Python 
## Objetivo: 
## Practicar el uso de Git con un proyecto Python desde la terminal: crear repositorio, 
editar archivos .py, commit, ramas, merge, push y stash. 
Requisitos: - Git instalado: https://git-scm.com/ - Cuenta en GitHub - Configurar Git con nombre y correo 
## Pasos: 
1. Crear una carpeta de proyecto: 
mkdir ProyectoPythonTerminal 
cd ProyectoPythonTerminal 
git init 
2. Crear archivo 'hola.py': 
echo "print('Hola desde la terminal')" > hola.py 
git add hola.py 
git commit -m "Primer commit con hola.py" 
3. Crear nueva rama 'feature/multiplicar': 
git checkout -b feature/multiplicar 
echo "def multiplicar(a, b): return a * b" > multiplicar.py 
git add multiplicar.py 
git commit -m "Agrega función multiplicar" 
4. Cambiar a main y hacer merge: 
git checkout main 
git merge feature/multiplicar 
5. Hacer push al repositorio remoto: 
Crear repo vacío en GitHub 
git remote add origin https://github.com/usuario/ProyectoPythonTerminal.git 
git push -u origin main 
6. Uso de stash (el comando git stash guarda los cambios modificados en el área de trabajo, 
incluyendo los archivos modificados, eliminados o creados, pero no confirmados, en un 
stash(un almacén temporal)):  
echo "# Cambios no guardados" > temporal.py 
git stash 


## Comandos enviados

C:\>mkdir ProyectoTerminal

C:\>cd ProyectoTerminal

C:\ProyectoTerminal>git init
Initialized empty Git repository in C:/ProyectoTerminal/.git/

C:\ProyectoTerminal>git --config global user.name "Mauricio Ortiz coronado"
unknown option: --config
usage: git [-v | --version] [-h | --help] [-C <path>] [-c <name>=<value>]
           [--exec-path[=<path>]] [--html-path] [--man-path] [--info-path]
           [-p | --paginate | -P | --no-pager] [--no-replace-objects] [--no-lazy-fetch]
           [--no-optional-locks] [--no-advice] [--bare] [--git-dir=<path>]
           [--work-tree=<path>] [--namespace=<name>] [--config-env=<name>=<envvar>]
           <command> [<args>]

C:\ProyectoTerminal>git config --global user.name "Mauricio Ortiz Coronado"

C:\ProyectoTerminal>git config --global user.mail  "303590844@cuc.cr"

C:\ProyectoTerminal>git init
Reinitialized existing Git repository in C:/ProyectoTerminal/.git/

C:\ProyectoTerminal>echo "print('Hola desde la terminal')" > hola.py 

C:\ProyectoTerminal>git add hola.py

C:\ProyectoTerminal>git commit -m "Agregar Hola.py"
[master (root-commit) fef89f6] Agregar Hola.py
 1 file changed, 1 insertion(+)
 create mode 100644 hola.py

C:\ProyectoTerminal>git checkout -b feature/multiplicar
Switched to a new branch 'feature/multiplicar'

C:\ProyectoTerminal>echo "def multiplicar(a,b): return a * b > multiplicar.py
"def multiplicar(a,b): return a * b > multiplicar.py

C:\ProyectoTerminal>git add multiplicar.py
fatal: pathspec 'multiplicar.py' did not match any files

C:\ProyectoTerminal>git commit -m "Agregar multiplicar"
On branch feature/multiplicar
nothing to commit, working tree clean

C:\ProyectoTerminal>echo "def multiplicar(a,b):return a + b">multiplicar.py

C:\ProyectoTerminal>git add multiplicar.py

C:\ProyectoTerminal>git commit -m "Agregar multiplicar"
[feature/multiplicar 92b2f03] Agregar multiplicar
 1 file changed, 1 insertion(+)
 create mode 100644 multiplicar.py

C:\ProyectoTerminal>git checkout main
error: pathspec 'main' did not match any file(s) known to git

C:\ProyectoTerminal>git checkout branch main
error: pathspec 'branch' did not match any file(s) known to git
error: pathspec 'main' did not match any file(s) known to git

C:\ProyectoTerminal>branch
'branch' is not recognized as an internal or external command,
operable program or batch file.

C:\ProyectoTerminal>git checkout main
error: pathspec 'main' did not match any file(s) known to git

C:\ProyectoTerminal>git branch
* feature/multiplicar
  master

C:\ProyectoTerminal>git checkout

C:\ProyectoTerminal>git branch
* feature/multiplicar
  master

C:\ProyectoTerminal>git checkout main
error: pathspec 'main' did not match any file(s) known to git

C:\ProyectoTerminal>git checkout ?
error: pathspec '?' did not match any file(s) known to git

C:\ProyectoTerminal>git checkout -b main
Switched to a new branch 'main'

C:\ProyectoTerminal>git merge feature/multiplicar
Already up to date.

C:\ProyectoTerminal>git remote add origin https://github.com/MauOrtizC/Terminal2

C:\ProyectoTerminal>git remote add origin https://github.com/MauOrtizC/Terminal
error: remote origin already exists.

C:\ProyectoTerminal>git remote add origin https://github.com/MauOrtizC/Terminal-Nueva
error: remote origin already exists.

C:\ProyectoTerminal>git remote add origin https://github.com/MauOrtizC/Terminal
error: remote origin already exists.

C:\ProyectoTerminal>git remote add origin https://github.com/MauOrtizC/Terminal-Nuevas.git
error: remote origin already exists.

C:\ProyectoTerminal>git remote add origin https://github.com/MauOrtizC/Terminal
error: remote origin already exists.

C:\ProyectoTerminal>git push -u origin main
remote: Repository not found.
fatal: repository 'https://github.com/MauOrtizC/Terminal2/' not found

C:\ProyectoTerminal>git remote add origin https://github.com/MauOrtizC/Terminal
error: remote origin already exists.

C:\ProyectoTerminal>git remote add origin https://github.com/MauOrtizC/Terminal2
error: remote origin already exists.

C:\ProyectoTerminal>git push -u origin main
To https://github.com/MauOrtizC/Terminal2
 ! [rejected]        main -> main (fetch first)
error: failed to push some refs to 'https://github.com/MauOrtizC/Terminal2'
hint: Updates were rejected because the remote contains work that you do not
hint: have locally. This is usually caused by another repository pushing to
hint: the same ref. If you want to integrate the remote changes, use
hint: 'git pull' before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.

C:\ProyectoTerminal>git pull
remote: Enumerating objects: 3, done.
remote: Counting objects: 100% (3/3), done.
remote: Total 3 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
Unpacking objects: 100% (3/3), 881 bytes | 176.00 KiB/s, done.
From https://github.com/MauOrtizC/Terminal2
 * [new branch]      main       -> origin/main
There is no tracking information for the current branch.
Please specify which branch you want to merge with.
See git-pull(1) for details.

    git pull <remote> <branch>

If you wish to set tracking information for this branch you can do so with:

    git branch --set-upstream-to=origin/<branch> main


C:\ProyectoTerminal>git branch --set-upstream-to=origin/<branch> main
The system cannot find the file specified.

C:\ProyectoTerminal>git pull
There is no tracking information for the current branch.
Please specify which branch you want to merge with.
See git-pull(1) for details.

    git pull <remote> <branch>

If you wish to set tracking information for this branch you can do so with:

    git branch --set-upstream-to=origin/<branch> main


C:\ProyectoTerminal>git push -u origin main
To https://github.com/MauOrtizC/Terminal2
 ! [rejected]        main -> main (non-fast-forward)
error: failed to push some refs to 'https://github.com/MauOrtizC/Terminal2'
hint: Updates were rejected because the tip of your current branch is behind
hint: its remote counterpart. If you want to integrate the remote changes,
hint: use 'git pull' before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.

C:\ProyectoTerminal>git pull
There is no tracking information for the current branch.
Please specify which branch you want to merge with.
See git-pull(1) for details.

    git pull <remote> <branch>

If you wish to set tracking information for this branch you can do so with:

    git branch --set-upstream-to=origin/<branch> main


C:\ProyectoTerminal>git pull main
fatal: 'main' does not appear to be a git repository
fatal: Could not read from remote repository.

Please make sure you have the correct access rights
and the repository exists.

C:\ProyectoTerminal>git remote add origin https://github.com/MauOrtizC/Terminal2
error: remote origin already exists.

C:\ProyectoTerminal>git push -u origin main
To https://github.com/MauOrtizC/Terminal2
 ! [rejected]        main -> main (non-fast-forward)
error: failed to push some refs to 'https://github.com/MauOrtizC/Terminal2'
hint: Updates were rejected because the tip of your current branch is behind
hint: its remote counterpart. If you want to integrate the remote changes,
hint: use 'git pull' before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.

C:\ProyectoTerminal>git checkout -b main
fatal: a branch named 'main' already exists

C:\ProyectoTerminal>git branch
  feature/multiplicar
* main
  master

C:\ProyectoTerminal>git checkout -b master
fatal: a branch named 'master' already exists

C:\ProyectoTerminal>git checkout -b master
fatal: a branch named 'master' already exists

C:\ProyectoTerminal>git branch master
fatal: a branch named 'master' already exists

C:\ProyectoTerminal>git pull 
There is no tracking information for the current branch.
Please specify which branch you want to merge with.
See git-pull(1) for details.

    git pull <remote> <branch>

If you wish to set tracking information for this branch you can do so with:

    git branch --set-upstream-to=origin/<branch> main


C:\ProyectoTerminal>git pull feature/multiplicar
fatal: 'feature/multiplicar' does not appear to be a git repository
fatal: Could not read from remote repository.

Please make sure you have the correct access rights
and the repository exists.

C:\ProyectoTerminal>git pull main
fatal: 'main' does not appear to be a git repository
fatal: Could not read from remote repository.

Please make sure you have the correct access rights
and the repository exists.

C:\ProyectoTerminal>git pull master
fatal: 'master' does not appear to be a git repository
fatal: Could not read from remote repository.

Please make sure you have the correct access rights
and the repository exists.

C:\ProyectoTerminal>git remote add origin https://github.com/MauOrtizC/Terminal.git
error: remote origin already exists.

C:\ProyectoTerminal>git remote add origin https://github.com/MauOrtizC/Terminal
error: remote origin already exists.

C:\ProyectoTerminal>git push -u origin main
To https://github.com/MauOrtizC/Terminal2
 ! [rejected]        main -> main (non-fast-forward)
error: failed to push some refs to 'https://github.com/MauOrtizC/Terminal2'
hint: Updates were rejected because the tip of your current branch is behind
hint: its remote counterpart. If you want to integrate the remote changes,
hint: use 'git pull' before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.

C:\ProyectoTerminal>git pull --rebase origin main
From https://github.com/MauOrtizC/Terminal2
 * branch            main       -> FETCH_HEAD
Successfully rebased and updated refs/heads/main.

C:\ProyectoTerminal>git push -u origin main
Enumerating objects: 7, done.
Counting objects: 100% (7/7), done.
Delta compression using up to 12 threads
Compressing objects: 100% (4/4), done.
Writing objects: 100% (6/6), 600 bytes | 600.00 KiB/s, done.
Total 6 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (1/1), done.
To https://github.com/MauOrtizC/Terminal2
   4d24654..1426129  main -> main
branch 'main' set up to track 'origin/main'.

C:\ProyectoTerminal>echo "# Cambios no guardados" > temporal.py 

C:\ProyectoTerminal>git stash
No local changes to save

C:\ProyectoTerminal>git stash apply
No stash entries found.

C:\ProyectoTerminal>git add temporal.py

C:\ProyectoTerminal>git stash
Saved working directory and index state WIP on main: 1426129 Agregar multiplicar

C:\ProyectoTerminal>git stash apply
On branch main
Your branch is up to date with 'origin/main'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   temporal.py

git stash apply 
Resultado esperado: manejo de control de versiones para scripts Python 
desde consola. 
