# Deň 3 — Procesy v Linuxe

## Čo som sa naučil
- Proces je bežiaci program (napr. bash, sshd, apache2).
- Každý proces má svoje PID (Process ID) a vlastníka.
- Signály slúžia na komunikáciu s procesmi (napr. SIGTERM, SIGKILL).

## Príkazy
- `ps` — zobrazí procesy aktuálneho terminálu.
- `ps aux` — zobrazí všetky procesy (aj iných užívateľov).
- `top` — live monitoring procesov (ukončenie cez `q`).
- `kill PID` — zdvorilo ukončí proces.
- `kill -9 PID` — nútené ukončenie procesu.
- `sleep 300 &` — spustí proces na pozadí (znak `&`).
- `ps aux | grep nazov` — nájde konkrétny proces podľa mena.
- `ps aux | less` — čítanie dlhého výstupu (ukončenie cez `q`).

## Praktické cvičenie
- Vyskúšal som `ps` a `ps aux`.
- Pozeral som `top` a naučil som sa z neho vystúpiť (`q`).
- Spustil som `sleep 300 &` na pozadí, našiel som jeho PID cez `grep` a ukončil ho cez `kill`.
- Naučil som sa používať `less` na čítanie dlhých výstupov.
