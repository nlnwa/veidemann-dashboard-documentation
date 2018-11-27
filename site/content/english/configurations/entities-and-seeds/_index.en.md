---
title: "Entities and seeds"
weight: 1
---

From entities and seeds a user can add and administrate web pages to harvest.

![Entities and seeds overview](/veidemann/docs/img/entities_and_seed/veidemann_dashboard_entities_and_seeds_overview.png)

#### Search
------------

The search bar on the page could be used to find an entity/seed with a matching name or label.
The icons shown in the list, will show where the match was found. 


Icon                                                                       | Hit 
---------------------------------------------------------------------------|---------
![entity icon](/veidemann/docs/img/entities_and_seed/veidemann_dashboard_entity_icon.png) | Entity
![seed icon](/veidemann/docs/img/entities_and_seed/veidemann_dashboard_seed_icon.png)     | Seed  
![label icon](/veidemann/docs/img/entities_and_seed/veidemann_dashboard_label_icon.png)   | Label


#### Entity {#entity}
---------------------

An entity in Veidemann is typically the owner of a web page, and consists of [metadata](../#veidemann-meta) and one or
more seeds.
  
#### Seed {#seed}
---------
A seed describes a web page that Veidemann should harvest, and must have a connecting entity.
It consist of [metadata](../#veidemann-meta), but in this implementation the *name* field is exchanged with URL. 
In addition, a seed consists of the field:

- **Entity ID**: The ID of the connected entity. The field is automatically generated when creating a new seed. 

- **On/Off**:   Decides if the seed should be harvested or not. 

- **Surt prefix**: Automatically generated based of the URL.

- **Job**: Defines what [crawljob](../crawljob) should be used to harvest the seed. 

