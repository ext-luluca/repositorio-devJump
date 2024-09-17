# Repositorio DevJump

## Comandos utilizados hasta ahora:

- Creación del repositorio en GitHub.
- Clonación del repositorio: `git clone https://github.com/tu-usuario/repositorio-devJump.git`
**Comando**: 
  ```bash
  git init
  git remote add origin <URL del repositorio>
  git pull origin main

# Se creó el archivo README.md para documentar los pasos.
# Se realizó el primer commit con el mensaje "Commit inicial".
git add README.md
git commit -m "Commit inicial con el README.md"
git push origin main

Ignorar archivos:
Se creó y configuró el archivo .gitignore.

echo "privado.txt" >> .gitignore
echo "privada/" >> .gitignore
git add .gitignore
git commit -m "Añadir .gitignore para ignorar privado.txt y la carpeta privada"

# Se creó la rama v0.2, se realizó un commit y se fusionó con main
git checkout -b v0.2
echo "Contenido de 1.txt" > 1.txt
git add 1.txt
git commit -m "Añadir fichero 1.txt en la rama v0.2"
git checkout main
git merge v0.2

# Se resolvió el conflicto entre las ramas main y v0.2
git checkout main
echo "Hola" >> 1.txt
git add 1.txt
git commit -m "Añadido Hola a 1.txt en main"
git checkout v0.2
echo "Adios" >> 1.txt
git add 1.txt
git commit -m "Añadido Adios a 1.txt en v0.2"
git checkout main
git merge v0.2
# Resolución de conflictos
git add 1.txt
git commit -m "Resuelto conflicto entre main y v0.2"

Se listaron ramas con y sin merge, y se configuró un alias para listar commits
git branch --merged
git branch --no-merged
git log --oneline --decorate --graph --all
git config --global alias.list 'log --oneline --decorate --graph --all'
git list

# Se eliminó la rama v0.2 local y en el repositorio remoto
git branch -d v0.2
git push origin --delete v0.2


