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



# Git Workflow (by Ulli)

​

## Generell

​

| Befehl                | Funktion                                         |

| --------------------- | ------------------------------------------------ |

| `git init`            | lokales Repository anlegen (init = initialize)   |

| `git status`          | Status des lokalen Repo anzeigen                 |

| `git log (--oneline)` | Log (komprimiert) anzeigen                       |

| `git restore`         | letzten Zustand aus remote Repo wiederherstellen |

​

## Verbinden eines lokalen Repo mit einem online Repo auf GitHub

​

1.  Repository auf GitHub anlegen

    - ohne README.md

    - gleicher Name wie lokales Repo

2.  **SSH** Adresse kopieren

​

         Vorsicht: Nicht die HTML Adresse!

​

3.  Von GitHub Befehle kopieren:

    - `git remote add origin (SSH)` (SSH link einfügen)

    - `git push -u origin main`

​

## Arbeiten auf Branches

​

Man sollte es vermeiden, Änderungen im Main Branch vorzunehmen

​

Alle features / chores / fixes sollten getrennt auf eigenen Branches entwickelt werden

​

Benennung: xxx/yyy mit xxx = Funktion (feature, chore, hotfix, bugfix etc.) und yyy = aussagekräftiger Name der vorgenommenen Änderungen

​

      Vorsicht:

      - Branchnamen nur einmal vergeben (auch nach erfolgreichem merge)

      - Keine Doppelpunkte im Branchnamen verwenden

​

- `git switch -c feature/new`: neuen Branch namens feature/new anlegen (-c = create) und in diesen hineinwechseln

- `git branch`: alle lokalen Branches anzeigen lassen

- `git branch -a`: alle lokalen und remote Branches anzeigen lassen

​

## Pull Request stellen

​

1. arbeiten auf Branch

2. regelmäßiges **committen** der Änderungen mit aussagekräftigen commit messages

   - `git add .`: alle Dateien des aktuellen Verzeichnis "stagen"

   - `git commit -m "xxx"`: Dateien mit einer aussagekräftigen Nachricht (-m = message) committen

3. mehrere commits während der Arbeit im Branch erstellen

4. `git push`: aktuellen Branch zu GitHub pushen

5. online auf GitHub Pull Request erstellen

6. Link des PRs auf Slack teilen und auf Reviews und den grünen Haken warten :)

7. online auf GitHub PR approven (mit "squash and merge commits")

​

## Lokales Repo nach erfolgreichem PR aktualisieren

​

Lokal (z.B. in VS Code) befindet man sich an dieser Stelle noch im Branch, das online Repo hat die Änderungen des Branches nach erfolgreich gemergtem PR aber schon im Main Branch

​

1. `git switch main`: im lokalen Repo auf den Main Branch wechseln

2. `git pull`: lokales Repo auf den Stand des GitHub Remote Repo setzen

3. `git branch -d feature/new`: den lokalen Branch namens feature/new löschen (die Änderungen sind ja im Main Branch integriert; der remote Branch wird auf GitHub gelöscht)

​

## Pull Request erstellen, falls der Main Branch sich zwischenzeitlich verändert hat

​

Es kann sein, dass man mehrere Branches bearbeitet, zeitlich benannt z.B. in Branch1 und Branch2. Beide werden vom gleichen Stand des Main Branch abgezweigt. Branch1 wird erfolgreich gemerged. Nun soll Branch2 gemerged werden, aber der Main Branch beinhaltet nun schon die Änderungen von Branch1 und unterscheidet sich somit vom Stand des Main Branch des lokalen Branch2.

​

Vorgehensweise:

​

1. `git switch main`: lokal zum (alten) Main Branch zurückkehren

2. `git pull`: Stand des GitHub Remote Repo ins lokale Repo holen

3. `git switch feature/branch2`: lokal zum Branch2 zurückkehren

4. `git merge main`: lokalen und (aktuellen) Main Branch zusammenführen

5. Pull Request für Branch2 erstellen (git add --> git commit --> git push)

​

## Pull Request lokal anschauen

​

1. `git clone (SSH link) (OrdnerName)`: remote Repository von GitHub mit dem SSH Link (SSH Link) wird in neuen Ordner namens (OrdnerName) geklont

2. `git branch -a`: lokale und remote branches anzeigen lassen

3. `git checkout (PRbranchName)`: Branch des PRs lokal herunterladen

4. `code .`: öffnen in VS Code


**How to fix: git problem mit** `**feature/branch-name:main**`  
Bei diesem Problem wollen wir den Upstream branch neu setzen, um eine korrekte Verbindung zwischen den beiden branches schaffen (ohne den remote main zu referenzieren). Das tun wir mit dem Befehl:  
`git push -u origin feature/branchname` und zwar während wir uns in dem feature branch befinden.  
Git luck ![:vierblättriges_kleeblatt:](https://a.slack-edge.com/production-standard-emoji-assets/14.0/apple-medium/1f340@2x.png)


- git restore (nicht git checkout -b !)
- git switch -c um neue Branches zu erstellen
- git fetch um nach neuen Branches zu suchen