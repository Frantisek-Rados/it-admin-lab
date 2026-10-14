# Deň 2 — Editácia súborov a práva

## Čo som sa naučil

### Nano
- Jednoduchý textový editor v termináli
- Ctrl+O = uložiť, Ctrl+X = zavrieť
- Používa sa na konfiguračné súbory a skripty

### Práva (permissions)
- Každý súbor má vlastníka, skupinu a práva
- Tri typy: r (read), w (write), x (execute)
- Tri kategórie: u (user), g (group), o (others)
- Čísla: r=4, w=2, x=1
- Bežné: 755 (skripty), 644 (súbory), 600 (súkromné), 700 (priečinky)

## Príkazy
- `nano subor` — otvor editor
- `chmod 755 subor` — zmeň práva na 755
- `chmod +x skript.sh` — pridaj právo spúšťania
- `chown user:group subor` — zmeň vlastníka
- `ls -l` — zobraz práva

## Praktické cvičenie
- Vytvoril som súbor v nano (`poznamka.txt`)
- Zmenil som práva na 600
- Napísal som prvý bash skript (`skript.sh`)
- Pridal som právo spúšťania
- Spustil som skript
- Zmenil som vlastníka na root a späť

## Problém s CRLF (Windows konce riadkov)
- Skript z Windows mal `\r\n` (CRLF) namiesto `\n` (LF)
- Bash nedokázal skript spustiť (chyba „Required file not found")
- Riešenie: `sed -i 's/\r$//' skript.sh`
- Overenie: `cat -A skript.sh` — na konci riadkov má byť len `$`, nie `^M$`

## Môj prvý skript

```bash
#!/bin/bash
echo "Ahoj, toto je môj prvý skript!"
echo "Dnes je: $(date)"
echo "Som užívateľ: $(whoami)"
