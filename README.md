# Flujo de trabajo con Gitflow

[CheatSheet de Gitflow](https://cheatography.com/guionardo/cheat-sheets/git-flow-and-git/pdf/)

## Clonar el repositorio

    git clone git@github.com:MYACCOUNT/MYREPO (SSH)
    ó
    git clone https://github.com/crisanto-lopez-gonet/taller-gitflow.git (HTTPS)


## Features
  
#### Crear feature branch a partir de develop:
    git checkout -b feature/nombreFeature develop

#### Hacer cambios/commits:
    git add <archivos>
    git commit -m "Cambio"

#### Comprobar que el merge funciona bien con develop:
    git checkout develop
    git pull
    git merge feature/nombreFeature
    
#### Se deshace el merge en develop:
    git reset --hard <commit_id>
    ó
    git reset --merge <commit_id>

#### Si el merge es OK, se sube la feature al repositorio:
    git checkout feature/nombreFeature
    git push -u origin feature/nombreFeature

#### ... se crea el PR en Github
#### Y se espera a que un compañero apruebe el PR  

---
#### Si el merge en develop no es OK ... Se deshace el merge:
    git reset --hard <commit_id>
    ó
    git reset --merge <commit_id>
    
    
    git checkout feature/nombreFeature

#### Se hacen los cambios para arreglar los conflictos o fallas:
    git add .
    git commit -m "Arreglados conflictos con develop"

#### Se suben los cambios:
    git push -u origin feature/nombreFeature

#### Y se crea el PR después de comprobar que la integración con develop será OK

