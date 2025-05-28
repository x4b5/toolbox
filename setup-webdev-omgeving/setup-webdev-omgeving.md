



> **Let op:**\
> Op deze (REA-)computer zijn **XAMPP** en **Git** al geïnstalleerd.\
> Gebruik de installatie-instructies hieronder alleen als je dit op een ander device wilt toepassen.

---

## 1. XAMPP installeren

Met XAMPP kun je websites en webapps lokaal ontwikkelen en testen, zonder dat je direct op een externe server hoeft te werken.

- Op deze computer is XAMPP al geïnstalleerd.
- Op een ander device: download [XAMPP](https://www.apachefriends.org/index.html) en installeer.
- Open het XAMPP Control Panel en start **Apache** (en eventueel MySQL).

---

## 2. Project-directory aanmaken op netwerkdrive


De Project-directory (project-map) op de Netwerkdrive maakt de directory toegankelijk vanaf meerdere computers, is veiliger en wordt regelmatig geback-upt.

- Maak op de **H:-schijf** (netwerkdrive) een projectmap aan, bijvoorbeeld `H:\mijn-project`.

---

## 3. Project-directory koppelen met XAMPP

- Virtuele hosts zijn niet mogelijk (geen admin-rechten).
- Pas de webroot aan naar jouw H:-map:
  1. Stop Apache via XAMPP Control Panel.
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
  5. Ga naar `http://localhost/` om je project te zien.

---

## 4. Git installeren

Git is een versiebeheersysteem die het mogeijk maakt om te veilig experimenteren en terug te gaan naar een vorige versie.

- Op deze computer is Git al geïnstalleerd.
- Op een ander device: download [Git](https://git-scm.com/) en installeer.
- Check installatie: open terminal/cmd en typ `git --version`.

---

## 5. GitHub-account aanmaken

GitHub biedt de mogelijkheid om je code online te bewaren, delen met anderen, en samenwerken aan projecten.

- Maak een account aan op [github.com](https://github.com/).

---

## 6. GitHub Desktop installeren

GitHub Desktop biedt de mogelijkheid om 

- Download en installeer [GitHub Desktop](https://desktop.github.com/).
- Log in met je GitHub-account.

---

## 7. Repository clonen

Repository (repo) clonen biedt de mogelijkheide om een laatste versie van een bestaand project te gebruiken

Clonen van de CodeCrashers-repo
- Open **GitHub Desktop**.
- Kies **File > Clone repository**.
- Zoek of plak de repo-URL, bijvoorbeeld  
  `https://github.com/CodeCrashersNL`
- Selecteer de locatie op je H:-schijf, bijvoorbeeld `H:\mijn-project`.
- Klik op **Clone**.

---

## 8. Repository aanmaken via GitHub Desktop

Met een repository kun je versiebeheer toepassen en je project eenvoudig synchroniseren met GitHub.


- Open GitHub Desktop.
- Kies **File > New repository**.
- Kies als Local path je H:-projectmap.
- Geef een naam en eventueel beschrijving.
- Voeg eventueel een README of .gitignore toe.
- Klik op **Create repository**.
- Klik op **Publish repository** voor upload naar GitHub (privé of publiek).

---

## 9. Opleidingscoaches (Collaborators) teogang geven tot repo



---

## 10. Repository committen en pushen via GitHub Desktop of VS-Code




## Setup testen

**Wat?**  
Zie [Setup testen](#begrippen).

**Waarom?**  
Zo weet je zeker dat alles goed is ingesteld en voorkom je problemen later.

**Hoe?**
- Open een browser en ga naar `http://localhost/`.
- Maak een kleine wijziging in je project.
- Commit & push via GitHub Desktop.
- Check of je wijziging zichtbaar is op github.com.

---

