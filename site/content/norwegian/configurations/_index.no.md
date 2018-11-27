---
title: "Konfigurasjoner"
pre: "<i class='fa fa-cog'></i>"
weight: 4
---

Veidemann Dashboard gir deg muligheten til å sette en rekke forskjellige konfigurasjoner for innhøstingen av websider.

I denne delen vil vi gå igjennom bruken av de ulike konfigurasjonene og parameterene som kan settes.  

I tabellen under vises alle tilgjengelige konfigurasjoner og en kort beskrivelse av hvilke oppgaver disse har.
For en mer utfyllende beskrivelse av deres funksjon, gå til siden for den aktuelle konfigurasjonen. 

#### Konfigurasjoner
--------------------  

Konfigurasjon                          | Beskrivelse
---------------------------------------|--------------------------------------------------------------------------------
[Entiter/Seeds](entities-and-seeds)    | Websider som skal høstes og konfigurering av disse 
[Crawljobs](crawljob)                  | Definerte jobber for innhøsting av websider.
[Schedule](schedule)                   | Setter tidspunkt for planlagte høstinger som brukes av crawljob.
[Crawlconfig](crawlconfig)             | Sett med innstillinger for høsteren som brukes av crawljob.
[Crawlhostgroup](crawlhostgroupconfig) | Opprett samlinger med IP-addresser som kan brukes av politeness. 
[Browserconfig](browserconfig)         | Innstillinger for nettleseren som brukes til høstingen. 
[Browserscript](browserscript)         | Scripts tilgjengelig for nettleseren brukt til høstingen.
[Politeness](politenessconfig)         | Høffligheten til høsteren
[Logging](logging)                     | Administrasjon av logging i Veidemann
[Brukere](users)                       | Administrasjom av brukere i systemet
[WARC status](warcstatus)              | Status for innhøstet materiale


#### Bruk av konfigurasjonssidene
----------------------------------
De fleste av konfigurasjonssidene er utformet likt, og består av to deler:  
- Liste over tilgjengelige konfigurasjoner.  
- Detaljer for en valgt konfigurasjon.

![configuration pages overview](/veidemann/docs/img/config/veidemann_dashboard_configuration_pages_overview.png)  

##### Opprette en konfigurasjon

En ny konfigurasjon av den valgte typen, opprettes ved å trykke på plussknappen oppe til høyre i bildet.
Et tomt skjema vil da dukke opp og data kan skrives inn.  Når kravet til påkrevde felter, og innholdet i disse
tilfredsstiller kravene, vil lagre-knappen på bunnen av siden bli tilgjengelig. Dersom et felt inneholder feil data,
vil en feilmelding vises under feltet.

{{% notice note %}}
Om flere konfigurasjoner er valgt, er det ikke mulig å opprette nye. Fjern markeringen for å starte opprettingen av en
konfigurasjon.
{{% /notice %}}


##### Tilgjengelige konfigurasjoner

Listen på toppen viser tilgjengelige konfigurasjoner av den valgte typen. Ved å klikke på en konfigurasjon i listen
vises detaljene for den valgte konfigurasjonen. Man vil da få muligheten til å redigere dataene eller slette
konfigurasjonen. Om man starter å redigere en konfigurasjon, kan denne tilbakestilles til sin opprinnelige stand ved å
trykke på tilbakestill-knappen.  


#### Gruppeoppdatering av konfigurasjoner
------------------------------------------
Flere av konfigurasjonene har støttet for gruppeoppdatering.
Veidemann dashboard har to forskjellige metoder for å oppdatere flere konfigurasjoner samtidig:    

1. Oppdatere et bestemt utvalg  
2. Oppdatere alle tilgjengelige konfigurasjoner

##### Oppdatere et bestemt utvalg
Om flere enn en konfigurasjon blir markert, blir det mulig 
å redigere feltene for disse bortsett fra metadata. Om et felt inneholder data betyr dette at dette feltet er likt for
alle de markerte. Om man oppdaterer et felt vil den nye verdien bli satt for alle de markerte, om feltet forblir tomt,
vil den opprinnelige verdien bli beholdt.  

{{% notice note %}}
Felter som har av/på verdier, vil bli deaktivert dersom alle de markerte ikke har lik verdi. For å sette et slikt felt
lik for alle må feltet trykkes på og deretter settes til ønsket verdi.
{{% /notice %}}

![config selected multiupdate](/veidemann/docs/img/config/veidemann_dashboard_configuration_selected_multiupdate.png)


##### Oppdatere alle tilgjengelige konfigurasjoner

Ved å trykke på boksen for å markere alle på siden, får man valget om markere alle tilgjengelige konfigurasjoner.
Dersom man velger dette vil absolutt alle konfigurasjonene av denne typen oppdateres. For dette tilfellet vil ikke
detaljevinduet vise om enkelte felter er like for alle valgte. Tomme felter her betyr at konfigurasjonen skal beholde 
sin opprinnelige verdi.

![config all on page selected](/veidemann/docs/img/config/veidemann_dashboard_all_configs_on_page_selected.png)

![config all configs selected](/veidemann/docs/img/config/veidemann_dashboard_all_configs_selected.png)


#### Meta {#veidemann-meta}
----------

Felles for de fleste av konfigurasjonene i Veidemann, er at de har tilhørende metedata som holder på grunnleggende
informasjon om konfigurasjonen.  

Innholdet i meta kan leses ut fra tabellen nedenfor.


![meta overview](/veidemann/docs/img/config/veidemann_dashboard_meta_overview.png)  


Felt                                      | Betydning
------------------------------------------|-----------------------------------------------------------------------------
[Navn](#meta-name)                        | Navn for konfigurasjonen
[Beskrivelse](#meta-description)          | Beskrivelse av konfigurasjonen
[Label](#meta-label)                      | Merkelapper for gruppering, søk osv.
[Opprettet](#meta-created)                | Dato for når konfigurasjonen ble opprettet
[Opprettet av](#meta-created-by)          | Navnet på brukeren som opprett konfigurasjonen
[Sist endret](#meta-last-modified)        | Dato for når konfigurasjonen ble sist endret
[Sist endret av](#meta-last-modiefied-by) | Navnet på brukeren som endret konfigurasjonen sist
[Id](#meta-id)                            | Et unikt nummer som identifiserer en bestemt konfigurasjon


##### Navn {#meta-name}
----------------------

Inneholder et egendefinert navn som kan brukes til å identifisere en konfigurasjon. Feltet er påkrevd 
og må minst bestå av to tegn. 

##### Beskrivelse {#meta-description}
------------------------------------

Inneholder en egendefinert beskrivelse av konfigurasjonen. Brukes til å gi konfigurasjonen en mer utfyllende tekst om
funksjon og bruksområde. Feltet er ikke påkrevd. 

##### Label {#meta-label}
------------------------

Labels er egendefinerte merkelapper som brukes til å markere konfigurasjonene med data som det ikke er laget felter for.
Eksempelvis kan en label brukes til gruppering av ulike konfigurasjone eller som et søkeord om man leter etter en
spesifikk konfigurasjon. 

![meta label](/veidemann/docs/img/config/veidemann_dashboard_meta_label.png)

En label består av et nøkkel/verdi-par på formen: **nøkkel:verdi**, og opprettes ved å trykke på linjen og skrive inn 
ønsket verdi på nevnte form og trykke enter.  

Eksisterende labels kan også redigeres eller slettes. Ved å trykke på en label vil man få muligheten til å redigere
nøkkel og verdi.

![meta edit label](/veidemann/docs/img/config/veidemann_dashboard_meta_edit_label.png)

##### Opprettet {#meta-created}
------------------------------
Inneholder dato i UTC for når konfigurasjonen ble opprettet. Feltet blir automatisk generert når det opprettes en ny
konfigurasjon.  

  
##### Opprettet av {#meta-created-by}
------------------------------------
Inneholder navnet eller e-postadressen til brukeren som opprettet konfigurasjonen. Feltet blir automatisk generert når
det opprettes en ny konfigurasjon.
   
    
##### Sist endret {#meta-last-modified}
--------------------------------------
Inneholder dato i UTC for når eg konfigurasjon ble sist endret. Feltet blir automatisk generert når en konfigurasjon
oppdateres.
  
      
##### Sist endret av {#meta-last-modified-by}
--------------------------------------------
Inneholder navnet eller e-postadressen til brukeren som oppdaterte konfigurasjonen sist. Feltet blir automatisk generert
når en konfigurasjon oppdateres.
  
    
##### Id {#meta-id}
-------------------
Inneholder en unik ID for konfigurasjonen. Feltet blir automatisk generert når en konfigurasjon opprettes.