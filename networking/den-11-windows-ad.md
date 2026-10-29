# Deň 11 — Windows Server a Active Directory

## Čo som sa naučil
- Active Directory (AD) je centrálna databáza používateľov a počítačov vo firme.
- Windows Server je OS, ktorý riadi AD, siete, tlačiarne a súbory.
- Domain Controller (DC) je server, na ktorom beží AD.
- AD umožňuje prihlásenie rovnakým heslom na akýkoľvek počítač v doméne.

## Príkazy (Linux a sieť)
- `ip a` — zobrazí IP adresy a sieťové rozhrania.
- `ping -c 4 google.com` — overí pripojenie na internet.
- `cat /etc/resolv.conf` — zobrazí DNS server.
- `smbclient -L localhost -N` — pokus o pripojenie k SMB serveru (Windows zdieľanie).

## Prečo je to dôležité pre pentestera
- AD je najčastejší cieľ útočníkov (ak hackneš AD, máš celú firmu).
- Pri penteste sa útočníci snažia zistiť, aké účty v AD existujú, a hľadajú tie s najvyššími právami.
- Znalosť Windows Servera a AD je nevyhnutná pre IT support aj pre pentestera.
