# HANDLEIDING SET-UP LOKALE WEBDEV-OMGEVING
**Versie 1 - 10 juni 2026**

><br>
> Niets zo frustrerend als je met volle energie ergens aan wilt beginnen, maar steeds vastloopt op technische hobbels. Daarom deze handleiding! In een paar duidelijke stappen zet je een webdevelopment-omgeving op en kun je snel van start met de opleiding.
>
>> De handleiding is vooral praktisch opgezet zodat je snel aan de slag kunt. Voor meer uitleg kun je op de links naar **[15. Meer weten](#15-meer-weten)** klikken.
>
>> De REA-computers draaien op het Windows-besturingssysteem. Deze handleiding is daarom specifiek voor Windows geschreven.
>
>> Voor het opzetten van je webdev-omgeving heb je onder andere XAMPP, Git en VS Code nodig. Deze zijn al geïnstalleerd op de REA-computer. 
De installatie-instructies worden hieronder benoemd als je dit op je eigen computer zou willen installeren.
>
>> Volg je het meeloop-programma? Je hebt alleen de eerste drie stappen van de handleiding nodig. Check ook eens **[14. Tools & Tricks](#14-tools--tricks)** voor handige tips en shortcuts die je workflow makkelijker maken.
>
>> Vragen, feedback, ideeën om deze handleiding beter te maken en actueel te houden? Laat het weten!
<br>

### INHOUD
##### [01. XAMPP installeren en Apache opstarten](#1-xampp-installeren-en-apache-opstarten)
##### [02. Projectmap aanmaken](#2-projectmap-aanmaken)
##### [03. Projectmap koppelen aan XAMPP](#3-projectmap-koppelen-aan-xampp)
##### [04. Git installeren](#4-git-installeren)
##### [05. GitHub-account aanmaken](#5-github-account-aanmaken)
##### [06. GitHub Desktop installeren](#6-github-desktop-installeren)
##### [07. Visual Studio Code installeren](#7-visual-studio-code-installeren)
##### [08. Repository clonen](#8-repository-clonen)
##### [09. Repository aanmaken via GitHub Desktop](#9-repository-aanmaken-via-github-desktop)
##### [10. Opleidingscoaches toegang geven tot je repo](#10-opleidingscoaches-toegang-geven-tot-je-repo)
##### [11. Lokale bestanden openen op localhost vanuit VS Code](#11-lokale-bestanden-openen-op-localhost-vanuit-vs-code)
##### [12. Repository-acties via GitHub Desktop of VS Code](#12-repository-acties-via-github-desktop-of-vs-code)
##### [13. Setup testen](#13-setup-testen)
##### [14. Tools & Tricks](#14-tools--tricks)
##### [15. Meer weten](#15-meer-weten)

---


### 1. XAMPP installeren en Apache opstarten
<br>
<img src="https://cdn2.iconfinder.com/data/icons/pack1-baco-flurry-icons-style/512/XAMPP.png" width="100" >
<br>
<br>

Met [#XAMPP](#xampp) kun je andere websites en webapps lokaal ontwikkelen en testen, zonder dat je direct op een externe server hoeft te werken. Apache is de module die dit mogelijk maakt. Hierdoor kun je snel, veilig en zelfstandig werken aan een project.


**XAMPP installeren:**

-   Op deze REA-computer is XAMPP al geïnstalleerd.
-   Op een andere computer installeren?: download [XAMPP](https://www.apachefriends.org/index.html) en installeer.

**Apache opstarten:**

-   Open het XAMPP Control Panel en start **Apache** via Actions-knop.

[🔝 Naar boven](#inhoud)

---

### 2. Projectmap aanmaken
<br>
<img src="https://cdn1.iconfinder.com/data/icons/files-server/24/Network_Drive-512.png" width="120" >
<br>
<br>

Een projectmap op de netwerkdrive (in dit geval de H:-schijf) maakt het mogelijk om toegang te hebben vanaf meerdere computers. Daarnaast wordt deze drive regelmatig geback-upt en is veiliger dan de lokale schijf.

-   Maak op de **H:-schijf** een projectmap aan, bijvoorbeeld `H:\mijn-project`.

[🔝 Naar boven](#inhoud)

---

### 3. Projectmap koppelen aan XAMPP
<br>
<img src="https://cdn0.iconfinder.com/data/icons/small-n-flat/24/678084-folder-512.png" width="100">
<br>
<br>

Als je projectmap niet op de C-drive staat, kun je XAMPP zo instellen dat het direct vanaf die map werkt:

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

[🔝 Naar boven](#inhoud)

---

### 4. Git installeren
<br>
<img src="https://cdn3.iconfinder.com/data/icons/social-media-2169/24/social_media_social_media_logo_git-512.png" width="100">
<br>
<br>


Git is een versiebeheersysteem waarmee je wijzigingen in projectbestanden kunt beheren, veilig kunt experimenteren, en kunt terugkeren naar een vorige versie.

-   Op deze computer is Git al geïnstalleerd.
-   Op een andere computer installeren?: download [Git](https://git-scm.com/) en installeer.
-   Checken of Git is geïnstalleerd (en weten welke versie van toepassing is)?: open terminal/cmd (Windows + R → typ `cmd`) en typ `git --version`.

[🔝 Naar boven](#inhoud)

---
### 5. GitHub-account aanmaken
<br>
|<img src="https://cdn4.iconfinder.com/data/icons/ionicons/512/icon-social-github-512.png" width="100">
<br>
<br>

GitHub biedt de mogelijkheid om je code online te bewaren, te delen met anderen, en samen te werken aan projecten.  
Daarvoor gebruik je een **repository** (repo): een projectmap waarin je bestanden én hun volledige versiegeschiedenis worden bijgehouden. Je kunt zo’n repo online aanmaken en synchroniseren tussen je **lokale projectmap en GitHub**.

-   Maak een account aan op [github.com](https://github.com/).

[🔝 Naar boven](#inhoud)

---

### 6. GitHub Desktop installeren
<br>
<img src= "https://cdn1.iconfinder.com/data/icons/social-circle-2-1/72/GitHub-512.png" width="100">
<br>
<br>

GitHub Desktop biedt de mogelijkheid om repo's te beheren via een grafische interface, zonder dat je de command line hoeft te gebruiken.  
Dit maakt het makkelijker om bewerkingen uit te voeren, vooral als je visueel wilt werken.

-   Download en installeer [GitHub Desktop](https://desktop.github.com/).
-   Log in met je GitHub-account.

[🔝 Naar boven](#inhoud)

---

### 7. Visual Studio Code installeren

<br>
<img src="https://cdn.iconscout.com/icon/free/png-512/visual-studio-code-1868944-1583105.png" width="100">
<br>
<br>

**Visual Studio Code (VS Code)** is een populaire en lichtgewicht code-editor van Microsoft, ideaal voor webontwikkeling.  
Het ondersteunt HTML, CSS, JavaScript, PHP, Git-integratie en nog veel meer via extensies.

**Installeren:**

-   Op deze computer is VS Code al geïnstalleerd.
-   Op andere computer installeren?: Download [VS Code](https://code.visualstudio.com/) en installeer.
-   Voeg eventueel de GitHub- of Live Server-extensie toe via de Extensions-markt (icoon links).

**Projectmap openen:**

-   Start VS Code.
-   Kies **File > Open Folder...** en selecteer je projectmap (bijv. `H:\mijn-project`).

[🔝 Naar boven](#inhoud)

---

### 8. Repository clonen

<br>
<img src= "https://cdn1.iconfinder.com/data/icons/system-basic-vol-9/20/copy-clone-file-512.png" width="100">
<br>
<br>

Een repo clonen maakt het mogelijk om (de laatste versie van) een bestaand project lokaal te gebruiken.

Clonen van de CodeCrashers-repo:

-   Open **GitHub Desktop**.
-   Kies **File > Clone repository**.
-   Zoek of plak de repo-URL, bijvoorbeeld  
    `https://github.com/CodeCrashersNL`
-   Selecteer de locatie op je H:-schijf, bijvoorbeeld `H:\mijn-project`.
-   Klik op **Clone**.

[🔝 Naar boven](#inhoud)

---

### 9. Repository aanmaken via GitHub Desktop

<br>
<img src="https://cdn-icons-png.flaticon.com/512/1828/1828919.png" width="100">
<br>
<br>

-   Open GitHub Desktop.
-   Kies **File > New repository**.
-   Kies als _Local path_ je H:-projectmap.
-   Geef een naam en eventueel een beschrijving.
-   Voeg eventueel een README of `.gitignore` toe.
-   Klik op **Create repository**.
-   Klik op **Publish repository** om deze te uploaden naar GitHub (privé of publiek).

[🔝 Naar boven](#inhoud)

---

### 10. Opleidingscoaches toegang geven tot je repo

<br>
<img src="https://cdn-icons-png.flaticon.com/512/1250/1250689.png" width="100">
<br>
<br>

Om je opdrachten na te laten kijken door de opleidingscoaches moet je hen toegang geven tot de repo.

-   Ga naar je repo op [github.com](https://github.com/).
-   Klik op het tabblad **Settings** (rechtsboven in de repo).
-   Kies **Collaborators and teams** in het menu aan de zijkant.
-   Klik op **Add people**.
-   Voeg de GitHub-accounts van de docenten toe.
-   De GitHub-accounts vind je in het Dashboard van CodeCrashers: klik op de knop `Team` en klik dan op het GitHub-icoontje boven de naam van de opleidingscoach. v
-   Kies `Read`-rechten.
-   Klik op **Add** en bevestig. v

[🔝 Naar boven](#inhoud)

---

### 11. Lokale bestanden openen op localhost vanuit VS Code

<br>
<img src="https://cdn-icons-png.flaticon.com/512/545/545682.png" width="100">
<br>
<br>

Om je site te testen in een realistischere omgeving (localhost) gebruik je de extension **Live Server** met live herlaadfunctie. Dit is noodzakelijk als je met JavaScript en API’s werkt, en gewoon handig voor HTML/CSS.

-   Installeer Live Server
-   Open bestand met sneltoets: `Alt+L` dan `Alt+O`

[🔝 Naar boven](#inhoud)

---

### 12. Repository-acties via GitHub Desktop of VS Code

<br>
<img src="https://cdn-icons-png.flaticon.com/512/32/32195.png" width="100">
<br>
<br>

Wanneer je aan je project werkt, pas je regelmatig bestanden aan. Om die wijzigingen op te slaan en bij te houden gebruik je een aantal acties.

-   **Committen**: je slaat je wijzigingen lokaal op in de versiegeschiedenis van je project. Je geeft bij elke commit een korte omschrijving (de _commit message_), zodat je later kunt terugzien wat je hebt aangepast en waarom.

-   **Pushen**: je stuurt je commits van je computer naar GitHub. Zo worden je aanpassingen online opgeslagen en eventueel gedeeld met je team.

-   **Pullen**: je haalt de laatste versie van het project van GitHub naar je eigen computer. Zo voorkom je dat je werkt met een verouderde versie.

Deze acties zorgen ervoor dat je veilig en gestructureerd kunt werken aan je project — je raakt niets kwijt, je kunt altijd terug in de tijd, en samenwerken wordt overzichtelijk en betrouwbaar.

**Via Terminal**
- Naviugeer naar repo-map: ```cd pad/naar/jouw/repository```
- Bekijk eventueel gewijzigde bestanden: ```git status```
- Voeg bestanden toe om te committen: ```git add .```
- Maak de commit met een bericht: ```git commmit -m "plaats hier je bericht"```
- Push de commit naar GItHub: ```git push origin main```




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

[🔝 Naar boven](#inhoud)

---

### 13. Setup testen

<br>
<img src="test.png" width="100">
<br>
<br>

Zo weet je zeker dat alles goed is ingesteld en voorkom je frustratie later.

-   Open een browser en ga naar `http://localhost/`.
-   Maak een kleine wijziging in een bestand.
-   Commit & push via GitHub Desktop.
-   Check of je wijziging zichtbaar is op github.com.

[🔝 Naar boven](#inhoud)

---

### 14. Tools & Tricks

<br>
<img src="tool-box.png" width="100">
<br>
<br>

**VS-Code**
-   **Sneltoetsen**

    -   Gebruik `Ctrl + Shift + P` voor het Command Palette.
    -   [Overzicht keyboard shortcuts for Windows](https://code.visualstudio.com/shortcuts/keyboard-shortcuts-windows.pdf)

- **Formatteren van code**
     - Gebruik `Shift + Alt + F` om je code netjes te laten inspringen en op te maken.

-   **Automatisch opslaan**
    -   Zet ‘Auto Save’ aan in VS Code (Bestand > Automatisch opslaan), zodat je wijzigingen niet verloren gaan.

-   **Drie belangrijke Extensions**
    - Prettier - Code formatter
Zorgt automatisch voor nette, consistente opmaak van je code, volgens standaard stijlgidsen.

    - Live Server
Start een lokale server waarmee je je HTML-pagina's direct in de browser kunt bekijken. Veranderingen in je code worden meteen zichtbaar.

    - ESLint
Controleert je JavaScript-code op fouten en waarschuwt voor slecht leesbare of foutgevoelige patronen. Helpt om schone en consistente code te schrijven.


**AI-tools**

We kunnen je natuurlijk niet tegenhouden om AI-tools te gebruiken. Sterker nog: AI zal een steeds belangrijkere rol spelen in webdevelopment. Maar waarom zijn we dan toch terughoudend?

Het doel van dit programma is dat je webdevelopment écht leert. Als je AI-tools inzet om een opdracht vooral maar zo snel mogelijk succesvol af te ronden, betekent dat nog niet dat je het onderliggende concept hebt begrepen of zelf zou kunnen toepassen.

Daarom: gebruik AI om te leren, niet om te ontwijken.
- Stel niet de vraag: “Geef me de juiste code.”
- Maar liever: "Leer me de juiste code schrijven voor deze opdracht?” of “Leg me stap voor stap uit hoe ik dit kan oplossen.”

**Referenties**
Hierbij 3 belangrijke en betrouwbare bronnen voor webdevelopment:
- [W3Schools](https://www.w3schools.com/)  
   *Praktische uitleg, voorbeelden en tutorials voor beginners tot gevorderden.*  
- [MDN Web Docs](https://developer.mozilla.org/)  
    *Uitgebreide documentatie en tutorials over webtechnologieën zoals HTML, CSS, JavaScript en meer.*  
- [Stack Overflow](https://stackoverflow.com/)  
    *Community voor het stellen van vragen en het vinden van antwoorden over programmeren.*




[🔝 Naar boven](#inhoud)

---
### 15. Meer Weten

<br>
<img src="bookworm.png" width="100">
<br>
<br>


##### #XAMPP
De letters van de naam XAMPP betekenen het volgende:  
_X = cross-platform:_ dit betekent dat XAMPP op verschillende besturingssystemen werkt.  
_A = Apache:_ hiermee draai je de lokale webserver.
_M = MySQL:_ Dit is de database. Voor nu niet relevant.  
_P = PHP:_ programmeertaal voor communicatie tussen server en database. Komt later aan bod.
_P = Perl:_ extra scripttaal maar komt niet aan bod in het leerprogramma.

[🔝 Naar boven](#inhoud)


