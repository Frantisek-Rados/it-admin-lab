# Deň 10 — Burp Repeater (Prvý skutočný test)

## Čo som sa naučil
- Repeater slúži na opakované posielanie a úpravu požiadaviek.
- Pomocou neho sa testujú zraniteľnosti (napr. SQL injection).
- Status Code 400 alebo 500 pri podozrivom znaku môže znamenať neošetrený vstup.

## Praktické cvičenie
- Poslal som požiadavku cez terminál: `curl -x http://127.0.0.1:8080 http://localhost`
- V HTTP history som ju poslal do Repeatera (pravé tlačidlo → Send to Repeater).
- Upravil som požiadavku: `GET /?test=1' HTTP/1.1` (pridal som apostrof).
- Server vrátil 400 Bad Request.

## Prečo je to dôležité pre pentestera
- Repeater je hlavný nástroj na hľadanie zraniteľností.
- Skúšaním rôznych znakov (', ", --) zistím, či server neošetruje vstup.
- Ak server vráti chybu (400/500) pri podozrivom vstupe, môže ísť o zraniteľnosť.
