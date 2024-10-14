# Liste over Cisco CCNA-kommandoer

## 1. `enable`
   - **Funktion**: Skifter fra brugerprompt (User Exec mode) til privilegeret mode (Privileged Exec mode), som tillader dig at udføre administrative kommandoer.
   - **Eksempel**:  
     ```
     Router> enable
     Router#
     ```

## 2. `configure terminal`
   - **Funktion**: Skifter til Global Configuration mode, hvor du kan foretage ændringer i enhedens konfiguration.
   - **Eksempel**:  
     ```
     Router# configure terminal
     Router(config)#
     ```

## 3. `interface`
   - **Funktion**: Går ind i konfigurationsmode for en specifik grænseflade (interface), hvor du kan konfigurere porte og netværksindstillinger.
   - **Eksempel**:  
     ```
     Router(config)# interface GigabitEthernet 0/1
     Router(config-if)#
     ```

## 4. `ip address`
   - **Funktion**: Bruges til at tildele en IP-adresse og subnetmaske til en specifik grænseflade.
   - **Eksempel**:  
     ```
     Router(config-if)# ip address 192.168.1.1 255.255.255.0
     ```

## 5. `no shutdown`
   - **Funktion**: Aktiverer en grænseflade, som som standard er slukket (shutdown) efter konfiguration.
   - **Eksempel**:  
     ```
     Router(config-if)# no shutdown
     ```

## 6. `show running-config`
   - **Funktion**: Viser den aktuelle konfiguration af enheden, herunder alle aktive indstillinger og parametre.
   - **Eksempel**:  
     ```
     Router# show running-config
     ```

## 7. `show ip interface brief`
   - **Funktion**: Viser en kort oversigt over alle interfaces og deres status (f.eks. om de er oppe eller nede) samt deres IP-adresser.
   - **Eksempel**:  
     ```
     Router# show ip interface brief
     ```

## 8. `ping`
   - **Funktion**: Tester netværksforbindelsen mellem den lokale enhed og en anden enhed ved at sende ICMP-pakker.
   - **Eksempel**:  
     ```
     Router# ping 192.168.1.2
     ```

## 9. `traceroute`
   - **Funktion**: Sporer ruten pakker tager til en specifik destination og viser hver hop undervejs.
   - **Eksempel**:  
     ```
     Router# traceroute 192.168.1.2
     ```

## 10. `copy running-config startup-config`
   - **Funktion**: Gemmer den aktuelle konfiguration (running config) som den permanente konfiguration (startup config), der bruges ved genstart.
   - **Eksempel**:  
     ```
     Router# copy running-config startup-config
     ```

## 11. `show ip route`
   - **Funktion**: Viser enhedens rutetabel, som indeholder information om, hvordan pakker skal sendes til forskellige destinationer.
   - **Eksempel**:  
     ```
     Router# show ip route
     ```

## 12. `router ospf`
   - **Funktion**: Konfigurerer OSPF (Open Shortest Path First) routing-protokollen på en router. Dette gør det muligt for en router at deltage i dynamisk routing ved hjælp af OSPF.
   - **Eksempel**:  
     ```
     Router(config)# router ospf 1
     ```

## 13. `network` (i routingprotokoller)
   - **Funktion**: Bruges i routing-protokoller som OSPF og EIGRP til at specificere netværk, der skal inkluderes i rutetabellen.
   - **Eksempel**:  
     ```
     Router(config-router)# network 192.168.1.0 0.0.0.255 area 0
     ```

## 14. `exit`
   - **Funktion**: Bruges til at afslutte en aktuel konfigurationsmode eller navigere op til en tidligere menu.
   - **Eksempel**:  
     ```
     Router(config-if)# exit
     ```

## 15. `reload`
   - **Funktion**: Genstarter enheden.
   - **Eksempel**:  
     ```
     Router# reload
     ```

## 16. `description`
   - **Funktion**: Tilføjer en beskrivelse til en grænseflade, hvilket gør det nemmere at identificere interfaces og deres funktion.
   - **Eksempel**:  
     ```
     Router(config-if)# description LAN to Switch 1
     ```

## 17. `ip route`
   - **Funktion**: Tilføjer en statisk rute i rutetabellen, som angiver, hvordan pakker skal dirigeres til en specifik destination.
   - **Eksempel**:  
     ```
     Router(config)# ip route 192.168.2.0 255.255.255.0 192.168.1.1
     ```

## 18. `switchport mode access`
   - **Funktion**: Konfigurerer en switch-port som en access-port, der tilhører et enkelt VLAN.
   - **Eksempel**:  
     ```
     Switch(config-if)# switchport mode access
     ```

## 19. `vlan`
   - **Funktion**: Opretter eller konfigurerer et VLAN (Virtual Local Area Network) på en switch.
   - **Eksempel**:  
     ```
     Switch(config)# vlan 10
     ```

## 20. `show mac address-table`
   - **Funktion**: Viser switchens MAC-adressetabel, som viser hvilke MAC-adresser der er knyttet til hvilke porte.
   - **Eksempel**:  
     ```
     Switch# show mac address-table
     ```
