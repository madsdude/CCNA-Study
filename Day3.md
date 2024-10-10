## OSI-modellen

**OSI (Open Systems Interconnection)** er en konceptuel model med syv lag, der standardiserer funktioner i netværk. Modellen hjælper med at kategorisere og strukturere netværksprotokoller og -standarder. Selvom OSI-modellen ikke er i praktisk brug i dag, er den vigtig i netværksteori og uddannelse.

### De 7 lag i OSI-modellen:
1. **Fysisk lag (Layer 1)**: Fysiske karakteristika af medierne (f.eks. kabler, signaler, volt).
2. **Datalink lag (Layer 2)**: Node-til-node forbindelse og dataoverførsel, bl.a. fejldetektion og rettelser. Switches arbejder på dette lag.
3. **Netværkslag (Layer 3)**: Sørger for forbindelser mellem forskellige netværk og indeholder IP-adressering. Routere arbejder på dette lag.
4. **Transportlag (Layer 4)**: Segmentering af data, reassemblering, og host-til-host kommunikation. Transmissionen kan være pålidelig (TCP) eller upålidelig (UDP).
5. **Sessionlag (Layer 5)**: Håndterer dialoger eller sessioner mellem systemer, opretholder, styrer og afslutter forbindelser.
6. **Præsentationslag (Layer 6)**: Oversætter data mellem applikations- og netværksformat. Inkluderer kryptering/dekryptering.
7. **Applikationslag (Layer 7)**: Interagerer med softwareapplikationer, såsom HTTP/HTTPS-protokoller, der bruges i browsere.

---

## TCP/IP-suite

**TCP/IP (Transmission Control Protocol/Internet Protocol)** er den netværksmodel, der bruges i moderne netværk (f.eks. internettet). Den har færre lag end OSI-modellen, men ligner OSI-strukturen.

### TCP/IP-modellens lag:
1. **Link-lag**: Tilsvarer OSI's datalink og fysiske lag.
2. **Internet-lag**: Tilsvarer OSI's netværkslag, ansvarlig for IP-adressering og routing.
3. **Transport-lag**: Tilsvarer OSI's transportlag, ansvarlig for host-til-host kommunikation (TCP/UDP).
4. **Applikationslag**: Samler OSI's applikations-, præsentations- og sessionlag.

---

## Dataens rejse gennem lagene (enkapsulering og deenkapsulering)

- **Enkapsulering**: Data, der sendes fra én enhed til en anden, gennemgår hvert lag i OSI-modellen og tilføjes en header på hvert lag.
- **Deenkapsulering**: Modtageren fjerner lagene i den omvendte rækkefølge, indtil det originale data er tilbage.

---

### Vigtige begreber:
- **PDU (Protocol Data Units)**:
  - Layer 4 → Segment (Transportlag)
  - Layer 3 → Packet (Netværkslag)
  - Layer 2 → Frame (Datalink-lag)
  - Layer 1 → Bit (Fysisk lag)
  
- **Same-layer interaction**: Kommunikation mellem samme lag på forskellige enheder.
- **Adjacent-layer interaction**: Samarbejde mellem lag på samme enhed.

---

## Quiz-notater:
- Same-layer interaction beskriver interaktion mellem samme lag på to forskellige værter.
- Enkapsuleringsproces: En frame består af tre headers (lag 4, 3, 2) og en trailer (lag 2).

Disse noter dækker de vigtigste koncepter i videoen. Skal jeg tilføje eller uddybe noget bestemt?
