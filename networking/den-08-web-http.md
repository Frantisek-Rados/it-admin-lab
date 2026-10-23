# Deň 8 — Ako funguje web a HTTP

## Čo som sa naučil
- HTTP je jazyk, ktorým komunikuje prehliadač so serverom (Request / Response).
- Request posiela prehliadač (napr. GET), Response posiela server (Status Code + HTML).
- Status kódy: 200 (OK), 301/302 (presmerovanie), 403 (zakázané), 404 (nenájdené), 500 (chyba servera).

## Príkazy
- `curl -I http://localhost` — zobrazí len hlavičky odpovede (Status Code, Server).
- `curl http://localhost` — zobrazí celý HTML kód stránky.

## Praktické cvičenie
- Nainštaloval som Apache (`sudo apt install apache2 -y`).
- Cez `curl -I http://localhost` som dostal `HTTP/1.1 200 OK`.
- Cez `curl -I http://localhost/neexistuje` som dostal `HTTP/1.1 404 Not Found`.
- Vo Firefoxe (F12 -> Network) som videl hlavičky a komunikáciu so serverom.

## Prečo je to dôležité pre pentestera
- Sledovaním HTTP kódov zistím, či server funguje, alebo či má chybu.
- Kód 403 alebo 500 môže znamenať skrytý priečinok alebo zraniteľnosť.
- HTTP je základ pre webové útoky (SQL injection, XSS).
