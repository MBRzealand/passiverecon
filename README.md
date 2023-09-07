# Passive Recon Assignment
Jeg har valgt at undersøge Novo Nordisk

## Domains og Subdomains
#### DNSdumpster
Vi kan kigge på DNSdumpster for at få kortlagt de forskellige domæner tilknyttet novo.
![image](https://github.com/MBRzealand/passiverecon/assets/70659124/0565799e-679f-4e9f-b3a0-2faa223c461b)

#### Google Dork
Vi kan ligeledes lave en google dork, hvor vi kan lede efter om der eksisterer nogen spændende subdomains.
![image](https://github.com/MBRzealand/passiverecon/assets/70659124/bf71ae8d-3561-49a5-ae92-6da40275c046)


## Teknologistack
#### DNSdumpster
**Fireeye** - en cloudbaseret email-tjeneste med henblik på at kunne stoppe ransomware og spear phishing  
**IIS 10.0** - betyder "Internet Information Services", er shipped med windows server 2016  
**ASP.NET** - serverside web framework til udvikling af dynamiske web applikationer  

#### Shodan.io
![image](https://github.com/MBRzealand/passiverecon/assets/70659124/4a2eece5-b70b-4acb-9fdf-0f811d3b3d2a)

## Foreslå nogle mulige attack vectors
#### Shodan.io
Hvis vi laver en hurtig sårbarhedsscanning på shodan for vi ingen hits. (```country:dk org:"Novo Nordisk" has_vuln:true```)  
Vi bemærker dog at en enkelt maskine på domænet ```aaftest001.novonordisk.com``` kører SSH på port 2222, dette ville være det bedste bud på en attack vector.  

## en vurdering af, hvorvidt du har fundet en honeypot eller en reel måske sårbar tjeneste

Shodan.io markerer automatisk systemer som honeypots, deraf vurderes ```aaftest001.novonordisk.com``` som en reel tjeneste, men den er dog ikke noteret som havende sårbarheder.

her kan vi se et eksempel på en honeypot hos TDC:  

![image](https://github.com/MBRzealand/passiverecon/assets/70659124/cf7842a0-cda2-4637-ad4f-d284df0f4e50)

