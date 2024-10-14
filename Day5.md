# Kursusintroduktion:

- Jeremy's IT Lab tilbyder en komplet CCNA-kursus, 100% gratis.
- Quiz og Anki flashcards er inkluderet for at styrke læringen.

# Emneoversigt:

- Fokuserer på Ethernet LAN-switching og OSI-modellens lag 1 (fysisk lag) og lag 2 (datablinklaget).

# OSI Model Gennemgang:

### Lag 1: Fysisk lag:
- Definerer de fysiske karakteristika for dataoverførsel.
- Eksempler inkluderer kabellængder (f.eks. UTP-kabler med en maksimal længde på 100 meter), elektriske signaler osv.

### Lag 2: Datablinklaget:
- Sikrer dataoverførsel fra en node til en anden.
- Bruger MAC-adresser (lag 2-adresser) til at forbinde enheder.
- Switches fungerer på lag 2.

# LAN Definition:

- LAN (Local Area Network) refererer til et netværk inden for et lille område, f.eks. et hjem eller kontor.
- Switche udvider LAN, men separerer det ikke. Routere forbinder separate LAN’er.

# OSI Model PDUs:

- Forskellige protokolenheder (PDUs) afhængigt af OSI-laget: Segment (lag 4), Pakke (lag 3), og Frame (lag 2).
- Ethernet rammer bruges til lag 2-protokoller.

# Ethernet Frame:

- **Header**: Indeholder Preamble, SFD, destination og kilde MAC-adresser, samt Type/Længde-felt.
- **Trailer**: Indeholder FCS (Frame Check Sequence) til fejlregistrering.

# MAC-adresser:

- MAC-adresser er 48-bit fysiske adresser tildelt ved fremstilling.
- Består af OUI (de første 3 bytes, som identificerer producenten) og en enhedsunik del (de sidste 3 bytes).

# Unicast og Frame-forwarding:

- Unicast rammer sendes til én specifik enhed.
- Switche lærer dynamisk MAC-adresser og bruger MAC-adressetabellen til at videresende rammer effektivt.
- Ukendte unicast-rammer oversvømmes til alle porte, indtil switchen lærer destinationens MAC-adresse.

# Frame Flooding og Forwarding:

- Ukendte unicast-rammer bliver floodet til alle porte undtagen den, hvor rammen kom fra.
- Når MAC-adresser er lært, videresendes rammer til den rigtige port.
