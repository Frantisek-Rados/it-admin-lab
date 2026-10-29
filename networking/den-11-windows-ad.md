# Deň 11 — Windows Server, Active Directory a Troubleshooting

## Čo som sa naučil
- Active Directory (AD) je centrálna databáza používateľov a počítačov vo firme.
- Windows Server je OS, ktorý riadi AD, siete, tlačiarne a súbory.
- Domain Controller (DC) je server, na ktorom beží AD.
- AD umožňuje prihlásenie rovnakým heslom na akýkoľvek počítač v doméne.

## Praktické cvičenie (Siete)
- `ip a` — zistil som svoju IP adresu (10.0.2.15) a bránu (10.0.2.2).
- `cat /etc/resolv.conf` — zistil som DNS server (127.0.0.53).
- `nslookup google.com` — overil som preklad domény na IP adresu.
- `ping -c 4 8.8.8.8` — overil som pripojenie na internet (0% packet loss).
- `nmap -p 80,443 localhost` — port 80 (HTTP) je otvorený, port 443 (HTTPS) je zatvorený.
- `smbclient -L localhost -N` — vyhodilo chybu NT_STATUS_CONNECTION_REQUIRED (SMB vyžaduje overenie).
- `ps aux | grep ssh` — nenašiel som sshd, ale gcr-ssh-agent.

## Troubleshooting (Riešenie problémov)
- Simuloval som výpadok webu (vypol som Apache cez `sudo systemctl stop apache2`).
- Zistil som, že stránka nejde (chyba Failed to connect).
- Skontroloval som stav služby cez `systemctl status apache2` (bolo tam inactive).
- Opravil som to cez `sudo systemctl start apache2`.
- Overil som, že to funguje cez `curl -I http://localhost` (vrátilo 200 OK).

## Prečo je to dôležité pre pentestera
- AD je najčastejší cieľ útočníkov (ak hackneš AD, máš celú firmu).
- Pri penteste sa útočníci snažia zistiť, aké účty v AD existujú, a hľadajú tie s najvyššími právami.
- Znalosť Windows Servera a AD je nevyhnutná pre IT support aj pre pentestera.
