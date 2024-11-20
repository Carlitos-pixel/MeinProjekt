# MeinProjekt


## Einrichten des GitHub-Repositorys 

1. Melde dich bei GitHub an.
2. Klicke oben rechts auf + > New repository.
3. Gib den Namen "MeinProjekt" ein.
4. Wähle Public oder Private aus.
5. Aktiviere ggf. die Option Add a README file.
6. Klicke auf Create repository.


## Erstellen eines SSH-Schlüssels

1. ssh-keygen -t ed25519 -C "mail@example.com"

2. Sobald der Schlüssel generiert ist, kopiere ihn in die Zwischenablage:
    cat ~/.ssh/id_ed25519.pub

3. Danach gehe dann zu GitHub und führe die folgenden Schritte aus:
   * Settings > SSH and GPG keys.
   * Click auf New SSH key.
   * Füge den Schlüssel ein und speichern.


## Projekt lokal einrichten

1. Öffne dein Terminal (Linux/Mac) oder Git Bash (Windows).

2. **Im gewünschten Ordner Repository klonen.**
    git clone https://github.com/username/repository-name.git

3. **In das Projektverzeichnis wechseln**
    cd repository-name

4. **Erstelle ein neues lokales Git-Repository.**
    git init

5. **Initieler Commit.**
    git add file-name
    git commit -m "Initialer Commit"

 ## Neuen Branch erstellen    
 1. **Lege einen neuen Branch namens "feature" an und wechsle zu diesem Branch**
    git checkout -b feature 

 2. **Eine weitere Datei hinzufügen (z. B. "utils/database.py") und einen Commit auf dem "feature"-Branch erstellen**
    git add utils/database.py
    git commit -m "Neue Funktion hinzugefügt"

## Branches mergen
 1. **Zum Main Branch wechseln.** 
    git checkout Main

 2. **Feature Branch nach Main mergen.**
    git merge feature

 3. **Merge Konflikt lösen**
    Auf "Resolve in  Merge editor" clicken  
    in "Result" den Code ändern und auf "Complete Merge" clicken

 4. **Führe den Merge-Vorgang ab, indem du die gelösten Konflikte commitest.**
    git commit -m "Merge von feature-Branch in Main-Branch" 

## Pushe dein lokales Git-Repository "MeinProjekt" an dein GitHub-Konto.
    git remote add origin https://github.com/username/MeinProjekt.git
    git push -u origin main
