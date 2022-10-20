#Git Vorgänge und Befehle

## zu Branch wechseln/erstellen

- git switch -c feature/new-content
- git add .
- git commit -m "Kommentar für commit"
- git push

## wenn es mal brenzlig wird

- git pull --no-ff
- git push -f

## branch löschen

- git branch -d feature/new-content