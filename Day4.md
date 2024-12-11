# Vigtige Begreber og Koncepter:

- **CLI (Command-Line Interface)**: Bruges til at konfigurere Cisco-enheder (routere, switches, firewalls).
- **Konsolport**: Metode til at forbinde en Cisco-enhed for at konfigurere den med CLI. Involverer normalt fysisk tilslutning af din laptop til enheden.
  - To typer konsolporte: **RJ45** og **USB mini-b**.
- **Rollover-kabel**: Bruges til RJ45-forbindelser (forskelligt fra et crossover-kabel).

# Terminalemulator og Indstillinger:

- **PuTTY**: En almindelig terminalemulator til at få adgang til Cisco CLI.
- **Serielle forbindelsesindstillinger** (standardindstillinger på Cisco-enheder):
  - Hastighed (baud rate): 9600 bits per sekund
  - Data bits: 8
  - Stop bit: 1
  - Paritet: Ingen
  - Flowkontrol: Ingen

# CLI-tilstande og Kommandoer:

- **User EXEC mode**: Begrænset adgang (indikator: '>').
- **Privileged EXEC mode**: Fuldt adgang til at vise og ændre enhedens konfiguration (indikator: '#'). Kommandoen til at få adgang er **enable**.
- **Global Configuration Mode**: Bruges til at ændre enhedens konfiguration (kommando: **configure terminal** eller **conf t**).

# Sikkerhed:

- ``Enable password``: Beskytter adgang til Privileged EXEC Mode med en adgangskode.
- ``Enable secret``: En mere sikker adgangskode, der er automatisk krypteret med MD5.
- ``Service password-encryption``: Krypterer adgangskoder, men med en svagere type kryptering end MD5.

# Konfigurationsfiler:

- **Running-config**: Den aktuelle, aktive konfiguration på enheden.
- **Startup-config**: Konfigurationen, der indlæses, når enheden genstartes.
  - Kommandoer til at gemme konfiguration: **write**, **write memory**, eller **copy running-config startup-config**.

# Annullering af Kommandoer:

- Skriv **no** foran en kommando for at annullere den.

# Opsummering af Vigtige Kommandoer:

- **enable**: For at komme i Privileged EXEC Mode.
- **configure terminal (conf t)**: For at komme i Global Configuration Mode.
- **show running-config**: Viser den aktuelle konfiguration.
- **show startup-config**: Viser den gemte opstartskonfiguration.

Disse notater giver en oversigt over, hvad der blev gennemgået i lektionen.
