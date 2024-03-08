# gitflow-test-1
agregando contenido de prueba en rama develop

# se comienza el flujo con instalando git flow, y creando el repositorio, y clonando a la pc
# luego se aplica el siguiente comando:

    git  flow init

    git branch develop
    git push -u origin develop

## para crear ramas de feature usamos el comando:
# via convencional

    git checkout develop 
    git checkout -b feature_branch

# via git flow

    git flow feature start feature_branch

## para finalizar la rama de feature
# via convencional

    git checkout develop 
    git merge feature_branch

# via git flow

    git flow feature finish feature_branch


## crear rama release
# via convencional

    git checkout develop 
    git checkout -b release/0.1.0

# via git flow

    git flow release start 0.1.0

## finalizar rama release
# via convencional
ß
    git checkout develop 
    git checkout -b release/0.1.0

# via git flow

    git flow release finish 0.1.0

## creacion rama hotfix
# via convencional

    git checkout main 
    git checkout -b hotfix_branch

# via git flow

    git flow hotfix start hotfix_branch

## finalizar rama hotfix se debe mezclar tanto en la rama develop como en la rama main (la rama main esta bloqueda por proteccion, se necesita hacer un pull request para poder mexclar)
# via convencional

    git checkout main 
    git merge hotfix_branch 

    git checkout develop 
    git merge hotfix_branch 

    git branch -D hotfix_branch

# via gitflow

    git flow hotfix finish hotfix_branch
