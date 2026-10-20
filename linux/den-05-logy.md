# Deň 5 — Logy a riešenie problémov

## Čo som sa naučil
- Logy sú textové záznamy o tom, čo sa v systéme deje (udalosti, chyby, prihlásenia).
- journalctl je nástroj na čítanie systémových logov (systemd).
- tail slúži na čítanie konca textových súborov.

## Príkazy
- `journalctl -xe` — zobrazí najnovšie logy a zvýrazní chyby (prvý príkaz pri riešení problému).
- `journalctl -u nazov_sluzby` — logy len pre konkrétnu službu (napr. apache2).
- `journalctl --since "10 minutes ago"` — logy za posledných 10 minút.
- `journalctl -f` — sledovanie logov naživo (ukončenie Ctrl+C).
- `tail -n 20 /var/log/syslog` — posledných 20 riadkov zo súboru.
- `tail -f /var/log/syslog` — sledovanie súboru naživo.

## Kde sú logy
- Všetky klasické logy sú v priečinku `/var/log/` (napr. `syslog`, `auth.log`).

## Čo hľadať v logoch (pre bezpečnosť)
- `Failed password` — neúspešné prihlásenie (možný brute-force útok).
- `Accepted password` — úspešné prihlásenie (skontroluj, či je oprávnené).
- `useradd` / `new user` — vytvorenie nového používateľa (možný backdoor).
- `sudo` / `COMMAND=` — zvýšenie práv (sleduj podozrivé príkazy).
- HTTP kódy 404, 403, 500 v Apache/Nginx — možné skenovanie webu alebo exploit.
- `Out of memory` — vyčerpanie RAM (možný DoS útok).

## Praktické cvičenie
- Prezrel som si najnovšie chyby cez `journalctl -xe`.
- Reštartoval som Apache a pozrel som si jeho logy cez `journalctl -u apache2`.
- Pozrel som si koniec systémového logu cez `tail -n 20 /var/log/syslog`.
