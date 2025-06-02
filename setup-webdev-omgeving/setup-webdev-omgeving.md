# SETUP WEBDEV-OMGEVING

> **Let op:**\
> Op deze (REA-)computer zijn **XAMPP** en **Git** al geïnstalleerd.\
> Gebruik de installatie-instructies hieronder alleen als je dit op een andere computer wilt toepassen.

---

## 1. XAMPP installeren

Met XAMPP kun je websites en webapps lokaal ontwikkelen en testen, zonder dat je direct op een externe server hoeft te werken. Hierdoor kun je snel, veilig en zelfstandig werken aan een project. De letters van de naam XAMPP betekenen het volgende:  
X = werkt op verschillende besturingssystemen  
A = Apache (lokale webserver)  
M = MySQL (database)  
P = PHP (programmeertaal voor communicatie tussen server en database)  
P = Perl (extra scripttaal maar komt niet aan bod in het leerprogramma)

- Op deze computer is XAMPP al geïnstalleerd.
- Op een andere computer installeren?: download [XAMPP](https://www.apachefriends.org/index.html) en installeer.
- Open het XAMPP Control Panel en start **Apache** (en eventueel MySQL).

---

## 2. Projectmap aanmaken op netwerkdrive

Een projectmap op de netwerkdrive (H:-schijf) is toegankelijk vanaf meerdere computers, wordt automatisch geback-upt en is veiliger.

- Maak op de **H:-schijf** (netwerkdrive) een projectmap aan, bijvoorbeeld `H:\mijn-project`.

---

## 3. Projectmap koppelen met XAMPP

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
5. Ga naar `http://localhost/` om je projectmap te bekijken.

Er bestaan ook andere manieren om een projectmap te koppelen met XAMPP, zoals virtual hosts (eigen domeinnaam koppelen aan de map) en symlinks (snelkoppeling naar je projectmap), maar deze vereisen in dit geval admin-rechten.

---

## 4. Git installeren

Git is een versiebeheersysteem waarmee je wijzigingen in projectbestanden kunt beheren, veilig kunt experimenteren, en kunt terugkeren naar een vorige versie.

- Op deze computer is Git al geïnstalleerd.
- Op een andere computer installeren?: download [Git](https://git-scm.com/) en installeer.
- Checken of Git is geïnstalleerd (en weten welke versie van toepassing is)?: open terminal/cmd (Windows + R → typ `cmd`) en typ `git --version`.

---

## 5. GitHub-account aanmaken

GitHub biedt de mogelijkheid om je code online te bewaren, te delen met anderen, en samen te werken aan projecten.  
Daarvoor gebruik je een **repository**: een projectmap waarin je bestanden én hun volledige versiegeschiedenis worden bijgehouden. Je kunt zo’n repository online aanmaken en synchroniseren tussen je **lokale projectmap en GitHub**.

- Maak een account aan op [github.com](https://github.com/).

---

## 6. GitHub Desktop installeren

GitHub Desktop biedt de mogelijkheid om repositories te beheren via een grafische interface, zonder dat je de command line hoeft te gebruiken.  
Dit maakt het makkelijker om bewerkingen uit te voeren, vooral als je visueel wilt werken.

- Download en installeer [GitHub Desktop](https://desktop.github.com/).
- Log in met je GitHub-account.

---

## 7. Repository clonen

Een repository (repo) clonen maakt het mogelijk om (de laatste versie van) een bestaand project lokaal te gebruiken.

Clonen van de CodeCrashers-repo:
- Open **GitHub Desktop**.
- Kies **File > Clone repository**.
- Zoek of plak de repo-URL, bijvoorbeeld  
`https://github.com/CodeCrashersNL`
- Selecteer de locatie op je H:-schijf, bijvoorbeeld `H:\mijn-project`.
- Klik op **Clone**.

---

## 8. Repository aanmaken via GitHub Desktop

- Open GitHub Desktop.
- Kies **File > New repository**.
- Kies als *Local path* je H:-projectmap.
- Geef een naam en eventueel een beschrijving.
- Voeg eventueel een README of `.gitignore` toe.
- Klik op **Create repository**.
- Klik op **Publish repository** om deze te uploaden naar GitHub (privé of publiek).

---

## 9. Opleidingscoaches (Collaborators) toegang geven tot repo

Als je samenwerkt met anderen, zoals opleidingscoaches, kun je hen toegang geven tot je repository.

- Ga naar je repo op [github.com](https://github.com/).
- Klik op het tabblad **Settings** (rechtsboven in de repo).
- Kies **Collaborators and teams** in het menu aan de zijkant.
- Klik op **Add people**.
- Voeg de GitHub-accounts van de docenten toe.
- De GitHub-accounts vind je in het Dashboard van CodeCrashers: klik op de knop `Team` en klik dan op het GitHub-icoontje boven de naam van de opleidingscoach.  v
- Kies `Read`-rechten.
- Klik op **Add** en bevestig. v

---

## 10. Repository committen en pushen via GitHub Desktop of VS Code

**Via GitHub Desktop:**
- Open de repository.
- Voeg een *commit message* toe (bijv. "Start project" of "Styling aangepast").
- Klik op **Commit to main**.
- Klik daarna op **Push origin** om te synchroniseren met GitHub.

**Via VS Code (indien Git is gekoppeld):**
- Ga naar het broncodebeheer-icoon links (met het tak-icoontje).
- Schrijf een commit message en klik op het vinkje (✓).
- Klik op **Synchronize Changes** of gebruik de Git-extensieknoppen.
- De melding 'There are no staged changes' betekent dat er geen wijzigingen zijn geselecteerd om te committen. 

---

## Setup testen

Zo weet je zeker dat alles goed is ingesteld en voorkom je frustratie later.

- Open een browser en ga naar `http://localhost/`.
- Maak een kleine wijziging in een bestand.
- Commit & push via GitHub Desktop.
- Check of je wijziging zichtbaar is op github.com.

---
