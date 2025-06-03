## HANDLEIDING SET-UP LOKALE WEBDEV-OMGEVING

> **Let op:**\
> Op deze REA-computer zijn **XAMPP**, **Git** en **VS Code** al geïnstalleerd.\
> Gebruik de installatie-instructies hieronder alleen als je dit op een andere computer wilt toepassen.

---
### INHOUD
[1. XAMPP installeren en Apache opstarten](#1-xampp-installeren-en-apache-opstarten)
[2. Projectmap aanmaken op netwerkdrive](#2.-projectmap-aanmaken-op-)

---


### 1. XAMPP installeren en Apache opstarten

<img src="https://cdn2.iconfinder.com/data/icons/pack1-baco-flurry-icons-style/512/XAMPP.png" width="100" >

Met XAMPP kun je andere websites en webapps lokaal ontwikkelen en testen, zonder dat je direct op een externe server hoeft te werken. Apache is de module die dit mogelijk maakt. Hierdoor kun je snel, veilig en zelfstandig werken aan een project.

De letters van de naam XAMPP betekenen het volgende:  
_X = cross-platform:_ dit betekent dat XAMPP op verschillende besturingssystemen werkt.  
_A = Apache:_ hiermee draai je de lokale webserver.
_M = MySQL:_ Dit is de database. Voor nu niet relevant.  
_P = PHP:_ programmeertaal voor communicatie tussen server en database. Komt later aan bod.
_P = Perl:_ extra scripttaal maar komt niet aan bod in het leerprogramma.

**XAMPP installeren:**

-   Op deze REA-computer is XAMPP al geïnstalleerd.
-   Op een andere computer installeren?: download [XAMPP](https://www.apachefriends.org/index.html) en installeer.

**Apache opstarten:**

-   Open het XAMPP Control Panel en start **Apache** via Actions-knop.

---

### 2. Projectmap aanmaken op netwerkdrive

<img src="https://cdn1.iconfinder.com/data/icons/files-server/24/Network_Drive-512.png" width="120" >

Een projectmap op de netwerkdrive (in dit geval de H:-schijf) maakt het mogelijk om toegang te hebben vanaf meerdere computers. Daarnaast wordt deze drive regelmatig geback-upt en is veiliger dan de lokale schijf.

-   Maak op de **H:-schijf** een projectmap aan, bijvoorbeeld `H:\mijn-project`.

---

### 3. Projectmap koppelen met XAMPP

<img src="https://cdn0.iconfinder.com/data/icons/small-n-flat/24/678084-folder-512.png" width="100">

Als je projectmap niet op de C-schijf staat, kun je XAMPP zo instellen dat het direct vanaf die map werkt:

1. Stop Apache via het XAMPP Control Panel.
2. Open `C:\xampp\apache\conf\httpd.conf` in Kladblok.
3. Zoek de regels:

    ```
    DocumentRoot "C:/xampp/htdocs"
    <Directory "C:/xampp/htdocs">
    ```

    en vervang deze door bijvoorbeeld:

    ```
    DocumentRoot "H:/mijn-project"
    <Directory "H:/mijn-project">
    ```

    4. Sla op en start Apache opnieuw.

4. Ga naar `http://localhost/` om je projectmap te bekijken.

Er bestaan ook andere manieren om een projectmap te koppelen met XAMPP, zoals virtual hosts (eigen domeinnaam koppelen aan de map) en symlinks (snelkoppeling naar je projectmap), maar deze vereisen in dit geval admin-rechten.

---

### 4. Git installeren

<img src="https://cdn3.iconfinder.com/data/icons/social-media-2169/24/social_media_social_media_logo_git-512.png" width="100">

Git is een versiebeheersysteem waarmee je wijzigingen in projectbestanden kunt beheren, veilig kunt experimenteren, en kunt terugkeren naar een vorige versie.

-   Op deze computer is Git al geïnstalleerd.
-   Op een andere computer installeren?: download [Git](https://git-scm.com/) en installeer.
-   Checken of Git is geïnstalleerd (en weten welke versie van toepassing is)?: open terminal/cmd (Windows + R → typ `cmd`) en typ `git --version`.

---

### 5. GitHub-account aanmaken

|<img src="https://cdn4.iconfinder.com/data/icons/ionicons/512/icon-social-github-512.png" width="100">

GitHub biedt de mogelijkheid om je code online te bewaren, te delen met anderen, en samen te werken aan projecten.  
Daarvoor gebruik je een **repository**: een projectmap waarin je bestanden én hun volledige versiegeschiedenis worden bijgehouden. Je kunt zo’n repository online aanmaken en synchroniseren tussen je **lokale projectmap en GitHub**.

-   Maak een account aan op [github.com](https://github.com/).

---

### 6. GitHub Desktop installeren

<img src= "https://cdn1.iconfinder.com/data/icons/social-circle-2-1/72/GitHub-512.png" width="100">

GitHub Desktop biedt de mogelijkheid om repositories te beheren via een grafische interface, zonder dat je de command line hoeft te gebruiken.  
Dit maakt het makkelijker om bewerkingen uit te voeren, vooral als je visueel wilt werken.

-   Download en installeer [GitHub Desktop](https://desktop.github.com/).
-   Log in met je GitHub-account.

---

---

### 7. Visual Studio Code installeren

<img src="https://cdn.iconscout.com/icon/free/png-512/visual-studio-code-1868944-1583105.png" width="100">

**Visual Studio Code (VS Code)** is een populaire en lichtgewicht code-editor van Microsoft, ideaal voor webontwikkeling.  
Het ondersteunt HTML, CSS, JavaScript, PHP, Git-integratie en nog veel meer via extensies.

**Installeren:**

-   Op deze computer is VS Code al geïnstalleerd.
-   Op andere computer installeren?: Download [VS Code](https://code.visualstudio.com/) en installeer.
-   Voeg eventueel de GitHub- of Live Server-extensie toe via de Extensions-markt (icoon links).

**Projectmap openen:**

-   Start VS Code.
-   Kies **File > Open Folder...** en selecteer je projectmap (bijv. `H:\mijn-project`).

---

### 8. Repository clonen

<img src= "https://cdn1.iconfinder.com/data/icons/system-basic-vol-9/20/copy-clone-file-512.png" width="100">

Een repository (repo) clonen maakt het mogelijk om (de laatste versie van) een bestaand project lokaal te gebruiken.

Clonen van de CodeCrashers-repo:

-   Open **GitHub Desktop**.
-   Kies **File > Clone repository**.
-   Zoek of plak de repo-URL, bijvoorbeeld  
    `https://github.com/CodeCrashersNL`
-   Selecteer de locatie op je H:-schijf, bijvoorbeeld `H:\mijn-project`.
-   Klik op **Clone**.

---

### 9. Repository aanmaken via GitHub Desktop

-   Open GitHub Desktop.
-   Kies **File > New repository**.
-   Kies als _Local path_ je H:-projectmap.
-   Geef een naam en eventueel een beschrijving.
-   Voeg eventueel een README of `.gitignore` toe.
-   Klik op **Create repository**.
-   Klik op **Publish repository** om deze te uploaden naar GitHub (privé of publiek).

---

### 10. Opleidingscoaches (Collaborators) toegang geven tot repo

Om je opdrachten na te laten kijken door de opleidingscoaches moet je hen toegang geven tot de repo.

-   Ga naar je repo op [github.com](https://github.com/).
-   Klik op het tabblad **Settings** (rechtsboven in de repo).
-   Kies **Collaborators and teams** in het menu aan de zijkant.
-   Klik op **Add people**.
-   Voeg de GitHub-accounts van de docenten toe.
-   De GitHub-accounts vind je in het Dashboard van CodeCrashers: klik op de knop `Team` en klik dan op het GitHub-icoontje boven de naam van de opleidingscoach. v
-   Kies `Read`-rechten.
-   Klik op **Add** en bevestig. v

---

## 11. Installeren en openen van bestanden op localhost vanuit VS Code

-   Installeer Live Server
-   Open bestand met sneltoets: `Alt+L` dan `Alt+O`

## 12. Repository-acties via GitHub Desktop of VS Code

Wanneer je aan je project werkt, pas je regelmatig bestanden aan. Om die wijzigingen op te slaan en bij te houden gebruik je een aantal acties.

-   **Committen**: je slaat je wijzigingen lokaal op in de versiegeschiedenis van je project. Je geeft bij elke commit een korte omschrijving (de _commit message_), zodat je later kunt terugzien wat je hebt aangepast en waarom.

-   **Pushen**: je stuurt je commits van je computer naar GitHub. Zo worden je aanpassingen online opgeslagen en eventueel gedeeld met je team.

-   **Pullen**: je haalt de laatste versie van het project van GitHub naar je eigen computer. Zo voorkom je dat je werkt met een verouderde versie.

Deze acties zorgen ervoor dat je veilig en gestructureerd kunt werken aan je project — je raakt niets kwijt, je kunt altijd terug in de tijd, en samenwerken wordt overzichtelijk en betrouwbaar.

**Via Terminal**

**Via GitHub Desktop:**

-   Open de repository.
-   Voeg een _commit message_ toe (bijv. "Start project" of "Styling aangepast").
-   Klik op **Commit to main**.
-   Klik daarna op **Push origin** om te synchroniseren met GitHub.

**Via VS Code (indien Git is gekoppeld):**

-   Ga naar het broncodebeheer-icoon links (met het tak-icoontje).
-   Schrijf een commit message en klik op het vinkje (✓).
-   Klik op **Synchronize Changes** of gebruik de Git-extensieknoppen.
-   De melding 'There are no staged changes' betekent dat er geen wijzigingen zijn geselecteerd om te committen.

---

## 13. Setup testen

Zo weet je zeker dat alles goed is ingesteld en voorkom je frustratie later.

-   Open een browser en ga naar `http://localhost/`.
-   Maak een kleine wijziging in een bestand.
-   Commit & push via GitHub Desktop.
-   Check of je wijziging zichtbaar is op github.com.

---

### 14. Praktische Tips

**VS-Code**
-   **Sneltoetsen**

    -   Gebruik `Ctrl + Shift + P` voor het Command Palette.
    -   [Overzicht keyboard shortcuts for Windows](https://code.visualstudio.com/shortcuts/keyboard-shortcuts-windows.pdf)

- **Formatteren van code**
     - Gebruik `Shift + Alt + F` om je code netjes te laten inspringen en op te maken.

-   **Automatisch opslaan**
    -   Zet ‘Auto Save’ aan in VS Code (Bestand > Automatisch opslaan), zodat je wijzigingen niet verloren gaan.

-   **Extensions**


**AI-tools**

- **ChatGPT**


- **GitHub Copilot (gratis versie)**
Met de gratis versie van GitHub Copilot krijg je elke maand een beperkt aantal AI-code-suggesties en chatberichten in Visual Studio Code.  
Na het installeren van de Copilot-extensie en inloggen met je GitHub-account kun je direct code-aanvullingen en hulpvragen gebruiken.  
Let op: zijn je maandelijkse limieten op, dan kun je Copilot die maand niet meer gebruiken.

- Open Visual Studio Code.
- Klik links in de zijbalk op het **Extensions**-icoon (vierkantje).
3. Zoek in het zoekveld bovenaan op: `GitHub Copilot`.
4. Klik op de extensie **GitHub Copilot** van GitHub.
5. Klik op **Install**.
6. Na installatie verschijnt er een melding om in te loggen.
7. Klik op **Sign in** en volg de stappen om in te loggen met je GitHub-account.
8. Na het inloggen is Copilot direct actief. Begin met coderen en je ziet automatisch AI-suggesties verschijnen.


**Documentatie**


