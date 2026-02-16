# Praktikprojekt


Kravspecifikationer
Systemet skal kunne:
- udføre ping mod enheder i netværket
- måle latency (svartider)
- registrere packet loss
- teste HTTP/HTTPS-forbindelser
- teste DNS-opslag
- scanne åbne TCP-porte
- registrere timeouts og manglende svar
- udføre tests automatisk med faste intervaller
- gemme målinger i en database
- vise status for enheder (online/offline)
- vise historik over målinger
- klassificere status som OK / Warning / Critical
- vise resultater i et webbaseret dashboard
- generere en rapport med målinger og status

4. Ikke-funktionelle krav

Systemet skal:
- kunne køre lokalt i et VM-baseret testmiljø
- være stabilt og ikke crashe ved fejl
- kunne håndtere manglende svar fra netværksenheder
- gemme data korrekt og konsistent i databasen
- være modulært opbygget, så nye tests kan tilføjes
- have en enkel og overskuelig brugerflade
- kunne udvides i senere udviklingsfaser

5. Afgrænsning
- Projektet udvikles som en prototype og afgrænses til:
- lokalt testmiljø (VMware)
- begrænset antal netværkstests
- ikke real-time overvågning
- ikke enterprise-løsning
- ikke integration til eksterne overvågningssystemer
- Fokus er på netværkstests, datalagring og visualisering.

6. Teknologier

Systemet udvikles med:
Backend:
Python
FastAPI

Frontend:
Streamlit

Database:
SQLite

Netværkstests:
ping
HTTP/HTTPS
DNS
portscan

Udviklingsmiljø:
VS Code
VMware testmiljø

7. Test og verifikation
Systemet verificeres gennem følgende tests:
- ping-test mod aktive enheder
- HTTP-test mod webserver
- portscan af testmaskiner
- DNS-opslag
- fejlscenarier (offline enheder / stoppede tjenester)

Systemet vurderes som fungerende når:
- tests gennemføres uden crash
- resultater registreres korrekt
- status vises korrekt i frontend
- data gemmes i database
