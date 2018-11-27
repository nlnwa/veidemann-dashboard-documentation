---
title: "Entiter og seeds"
weight: 1
---


Fra entiter og seeds kan man legge til og administrere nettsteder som skal høstes. 

![Entities and seeds overview](/veidemann/docs/img/entities_and_seed/veidemann_dashboard_entities_and_seeds_overview.png)

#### Søk
-------

For å finne frem til en entitet/seed kan søket på siden benyttes. Søket vil prøve å finne match i navnet til en entitet 
eller seed, og i labels.  
Ikonene i listen viser hvor søket har funnet match.  


Ikon                                                                       | Treff 
---------------------------------------------------------------------------|---------
![entity icon](/veidemann/docs/img/entities_and_seed/veidemann_dashboard_entity_icon.png) | Entitet
![seed icon](/veidemann/docs/img/entities_and_seed/veidemann_dashboard_seed_icon.png)     | Seed  
![label icon](/veidemann/docs/img/entities_and_seed/veidemann_dashboard_label_icon.png)   | Label


#### Entitet {#entity}
------------

En entiet i Veidemann er typisk en eier av nettsted, og består av [metadata](../#veidemann-meta) og en eller flere 
seeds.

#### Seed {#seed}
---------

En seed beskriver ett nettsted som Veidemann skal høste, og må være tilknyttet en entiet. 
Den består av [metadata](../#veidemann-meta), men i denne implementasjonen er navn byttet ut med URL. 
Ellers består en seed av feltene:

- **Entietens ID**: Id til entiteten seeden er tilknyttet. Feltet blir generert automatisk ved oppretting av en ny seed.


- **Av/På**: Bestemmer om seeden skal høstes eller ikke.  

- **Surt prefiks**: Feltet blir automatisk generert av URL.

- **Jobb**: Bestemmer hvilken [crawljob](../crawljob) som skal brukes til å høste seeden.

