# Deň 4 — Služby v Linuxe

## Čo som sa naučil
- Služba je program, ktorý beží na pozadí a spúšťa sa automaticky pri štarte.
- systemd je systémový manažér, systemctl je príkaz na jeho ovládanie.

## Príkazy
- `systemctl status nazov` — stav služby (running/inactive)
- `sudo systemctl start nazov` — spustí službu
- `sudo systemctl stop nazov` — zastaví službu
- `sudo systemctl restart nazov` — reštartuje službu
- `systemctl is-enabled nazov` — zistí, či sa spustí pri boote (enabled/disabled)
- `sudo systemctl enable nazov` — zapne auto-štart
- `systemctl list-units --type=service` — zoznam všetkých služieb

## Praktické cvičenie
- Skontroloval som stav služby `ssh` a skúsil som ju zastaviť a spustiť.
- Nainštaloval som webový server `apache2` cez `apt`.
- Overil som, že Apache funguje cez príkaz `curl http://localhost` (vyplul HTML kód).
- Zistil som, že keď Apache zastavím, `curl` vyhodí chybu.
