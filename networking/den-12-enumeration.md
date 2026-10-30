# Deň 12 — Prieskum siete a zraniteľností (Enumeration)

## Čo som sa naučil
- Enumeration je fáza, kedy hacker zisťuje, čo sa v systéme a sieti nachádza.
- Zisťujeme: aké počítače tam sú, akých používateľov, aké zdieľané priečinky a služby.
- Tieto informácie sa potom používajú pri útoku (napr. hľadanie zraniteľných verzií).

## Praktické cvičenie (Príkazy)
- `ip neigh` — zobrazí zariadenia v sieti (IP a MAC adresy).
- `cat /etc/passwd` — zobrazí zoznam používateľov v systéme (našiel som ich cca 30).
- `who` — zobrazí, kto je práve prihlásený.
- `smbclient -L localhost -U%` — pokus o pripojenie k Windows zdieľaniu (vyhodilo NT_STATUS_CONNECTION_REFUSED, čo je normálne, keď SMB na Linuxe nebeží).
- `nmap -sV -p 1-1000 localhost` — oskenuje porty a zistí služby (našiel som port 80 - Apache, port 631 - CUPS).

## Zistenie citlivých súborov
- `cat /etc/passwd | grep -v nologin` — zobrazí reálnych používateľov (našiel som 10).
- `sudo cat /etc/shadow` — zobrazí zašifrované heslá (hash). Toto by hacker chcel získať, aby mohol heslá lúskať.

## Prečo je to dôležité pre pentestera
- Ak zistím, že na porte 631 beží CUPS 2.4, môžem v databáze CVE hľadať známe chyby.
- Ak nájdem zdieľaný priečinok, môžem z neho získať dáta.
- Ak získam `/etc/shadow`, môžem sa pokúsiť prelúskať heslá a prihlásiť sa ako administrátor (root).

## Troubleshooting (simulácia)
- Skúsil som sa prepnúť na roota cez `su - root`.
- Systém mi vrátil `Authentication failure` (lebo som nezadal správne rootove heslo).
- Zistil som, že heslá musia byť silné (nestačí 123456).
