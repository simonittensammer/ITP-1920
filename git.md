# Git

VCS ... Version Contol System (Versionierungssystem)

## Probleme / Anforderungen

- Die Codebasis muss regelmäßig gesichert werden.
- Der Entwickler möchte Zugriff auf ältere Versionen seines Programms haben.
- Meistens werden Softwareprodukte in Teams erstellt; jedes Teammitglied braucht Zugriff auf den Sourcecode
- Teammmitglieder arbeiten oft gleichzeitig an den selben Sourcecode-Files. Sämtliche Änderungen müssen in die Codebasis eingepflegt werden.
- Separates Entwickeln von neuen Features, bis diese fehlerfrei sind und anschließendes Einfügen dieser neuen Funktionen in die Codebasis

## Alternativen

Sind ungenügend:

- regelmäßiges zippen der Codebasis und sichern
- zur Verfügung stellen der Codebasis auf einem File-Server und /oder auf der Dropbox (oder vergleichbare Dienste)

## Aufbau

- zentrale VCS zB Subversion
- dezentrale VCS zB Git

Provider: GitHub, Bitbucket, Gitlab


## Anwendungsfälle

### Erstellen eines Projekts

```
git init
```

#### Leeres Projekt aus Git-Repo clonen

```
git clone [ project-url ]
```

#### Bereits bestehendes Projekt ins Git-Repo commiten

```
git add [ your files / . ]
git commit -m "[ comment ]"
git remote add origin [ repo url ]
git push -u origin master
```

### Ein Projekt aus dem Repos downloaden (clonen)

```
git clone [ project-url ]
```

### Neue und/oder geänderte Dateien ins das Repo einpflegen

```
git add [ your files / . ]
git commit -m "[ comment ]"
git remote add origin [ repo url ]
git push -u origin master
```

#### Dateien in die Staging Area einpflegen

```
git add [ your files / . ]
```

#### Dateien aus der Staging Area entfernen

```
git reset [ your files / . ]
```

#### Dateien in das local-repo einpflegen

```
git add [ filename ]
```

#### Dateien aus dem local-repo entfernen

```
git rm [ filename ]
```

#### Dateien in das remote-repo einpflegen

```
git commit [ filename / . ]
```

#### Dateien aus dem remote-repo entfernen

```
git remote rm [ filename ]
```

### Status des Git-Working-Directories ansehen

```
git status
```

### Pretty Printing für Git-Logs

```
git log --all --decorate --oneline --graph
```

### Zweige für eigene Features erstellen

```
git branch [ branchname ]
```

### Branch wechseln

```
git checkout [ branchname ]
```

### Branch mergen

```
git merge [ branchname ]
```

### Pull requests durchführen

```
git request-pull <start> [ repo url ] <end>
```

### Commits taggen

Szenario: Die einzelnen Releases (zB bei Auslieferung an den Kunden) sollen getagged werden

Begriff der Baseline

### Einen Release-Eintrag im Github erstellen (inkl. Doku)

### Verwerfen der lokalen Änderungen

Was bedeutet `stash`