# Deň 6 — Siete základy (IP, DNS, DHCP)

## Čo som sa naučil
- IP adresa je adresa zariadenia v sieti (napr. 10.0.2.15).
- DNS je "telefónny zoznam internetu" – prekladá doménové mená (google.com) na IP adresy.
- DHCP automaticky prideľuje IP adresy zariadeniam v sieti.
- Súkromné IP adresy (napr. 10.x.x.x, 192.168.x.x) nie sú viditeľné z internetu.

## Príkazy
- `ip a` — zobrazí IP adresy a sieťové rozhrania.
- `ping -c 4 google.com` — overí pripojenie na internet (pošle 4 správy).
- `cat /etc/resolv.conf` — zobrazí nastavenie DNS servera.

## Praktické cvičenie
- Zistil som svoju IP adresu cez `ip a` (10.0.2.15/24).
- Overil som pripojenie na internet cez `ping -c 4 google.com` (0% packet loss).
- Zistil som, že môj lokálny DNS server je 127.0.0.53 (systemd-resolved).
