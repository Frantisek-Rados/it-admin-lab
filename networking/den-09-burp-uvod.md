# Deň 9 — Burp Suite (Úvod)

## Čo som sa naučil
- Burp Suite je nástroj na zachytávanie a úpravu HTTP komunikácie.
- Funguje ako proxy medzi prehliadačom (alebo terminálom) a serverom.
- Intercept ON = Burp zastaví požiadavku a čaká na moje povolenie (Forward).
- Intercept OFF = Burp len ticho sleduje komunikáciu.
- HTTP history = zoznam všetkých požiadaviek, ktoré cez Burp prešli.

## Nastavenie
- Nainštaloval som Burp Suite v Ubuntu.
- Vo Firefoxe som nastavil proxy: 127.0.0.1, port 8080 (aj pre HTTPS).
- Zistil som, že ak prehliadač blbne s HTTPS, dá sa to obísť cez terminál.

## Praktické cvičenie
- Zachytil som prvú HTTP požiadavku (GET).
- Poslal som požiadavku cez terminál: `curl -x http://127.0.0.1:8080 http://localhost`
- V Burpe v záložke "HTTP history" som videl záznam o tejto požiadavke a mohol som si pozrieť Request a Response.

## Prečo je to dôležité pre pentestera
- Burp je najpoužívanejší nástroj na testovanie webovej bezpečnosti.
- Pomocou histórie a úpravy požiadaviek sa robia útoky ako SQL injection alebo XSS.
- Toto je prvý krok k reálnemu hackovaniu webov.
