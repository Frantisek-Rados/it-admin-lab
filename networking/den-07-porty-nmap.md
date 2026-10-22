# Deň 7 — Porty a skenovanie (Nmap)

## Čo som sa naučil
- Port je číslo, ktoré určuje, aká služba beží na danej IP adrese.
- Bežné porty: 22 (SSH), 80 (HTTP), 443 (HTTPS), 631 (CUPS tlač).
- Nmap je nástroj na skenovanie portov a zisťovanie zraniteľností.
- Antivírus môže blokovať Nmap, ak skenuje cez sieť. Skenovanie localhost je bezpečné.

## Príkazy
- `nmap IP_adresa` — oskenuje základné porty na danej IP.
- `nmap -sV IP_adresa` — oskenuje porty a zistí verzie služieb.
- `sudo nmap -O IP_adresa` — oskenuje a zistí operačný systém.
- `nmap localhost` — oskenuje tvoj vlastný počítač.
- `nmap -p 1-100 localhost` — oskenuje len porty v rozsahu 1-100.
- `sudo nmap -A localhost` — agresívne skenovanie (OS, verzie, skripty, robots.txt).
- `nmap -Pn localhost` — skenovanie bez pingnutia.

## Praktické cvičenie
- Nainštaloval som Nmap (`sudo apt install nmap -y`).
- Oskenoval som `localhost` cez `nmap localhost`. Výsledok: port 631 (CUPS 2.4) je otvorený. 999 portov je zatvorených.
- Cez `nmap -A localhost` som našiel: `robots.txt`, simulovanú Network Camera a ASUS RT-N56U WAP (router).
- Toto je prvá fáza hackingu: Reconnaissance (prieskum).

## Prečo je to dôležité pre pentestera
- Skenovanie portov je prvý krok pri hľadaní zraniteľností.
- Ak nájdem otvorený port, zistím verziu služby a hľadám známe chyby (CVE).
