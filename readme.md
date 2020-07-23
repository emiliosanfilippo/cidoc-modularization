# Modularization of CIDOC CRM

This repository contains an experimental library of OWL ontologies based on the modularization of the **Erlangen release** (https://github.com/erlangen-crm/ecrm) of **CIDOC CRM** (v.6.2.1) (http://www.cidoc-crm.org/releases_table).

The library of modular ontologies is in the testing phase.


## Repository overview

The reader can refer to the figures in the folder **Diagrams** which graphically show how CIDOC's classes are distributed across the various modules.

**Cross-functional modules**

* **cidoc:place-module.owl**: it represents places (*E53 Place*);

* **cidoc:dimension-module.owl**: it represents dimensions (*E54 Dimension*); the new class *Qualitative Quality Space* allows for the representation of dimensions' qualitative values in addition to quantitative values; the latter are represented with OWL data properties.


**Modules about persistent items**

* **cidoc:persistent-item-top-module.owl**, see yellow classes in Fig.1: this module covers the most general classes about persistent items; its purpose is to allow for the consistent integration of all modules about persistent items;

* **cidoc:physical-thing-module.owl**, see green classes in **Fig.1**: it represents non-man-made physical things, e.g., *E19 Physical Object* and *E26 Physical Feature*;

* **cidoc:artifact-module.owl**, see red classes in **Fig.1**: it represents physical man-made entities, e.g., *E22 Man-Made Object*, *E25 Man-Made Feature*, and *E78 Collection*;

* **cidoc:actor-module.owl**, see blue classes in **Fig.1**: it represents actors, e.g., *E21 Person* and *E74 Group*;

* **cidoc:concept-module.owl**, see violet classes in **Fig.1**: it represents non-physical conceptual entities, i.e, *E28 Conceptual Object* and all its subclasses; the development of this module requires further work;


**Modules about temporal entities**

* **cidoc:temporal-entity-top-module**, see white classes in **Fig.2**: it covers the most general classes about temporal entities; its purpose is to allow for the consistent integration of all modules about temporal entities;

* **cidoc:actor-activity-module**, see green classes in **Fig.2**: it represents activities related to either the life or death of individual actors (e.g., *E67 Birth*, *E69 Death*), or to groups and legal bodies (e.g., *E86 Leaving*, *E66 Formation*, *E68 Dissolution*, etc);

* **cidoc:attribute-assignment-activity-module**, see class in violet in **Fig.2**: it represents activities for attributes assignment (e.g., *E13 Attribute Assignment* and its subclasses);

* **cidoc:creation-activity-module**, see grey class in **Fig.2**: it represents the creation of conceptual objects (*E65 Creation*); this module deserves further development;

* **cidoc:cultural-heritage-activity-module**, see blue classes in **Fig.2**: it represents temporal entities relative to cultural heritage (e.g., *E87 Curation Activity*);

* **cidoc:modification-activity-module**, see yellow classes in **Fig.2**: it represents the production, modification, or destruction of physical entities (e.g., *E79 Part Addition*, *E6 Destruction*, etc.);

* **cidoc:move-activity-module**, see red class in **Fig.2**: it represents the movement of physical objects (*E9 Move*);

**Integrating modules**: the following modules are used to integrate the ones presented above

* **temporal-whole-module.owl**: it imports all modules about temporal entities;

* **persistent-whole-module.owl**: it imports all modules about persistent items;

* **cidoc-whole.owl**: it imports all modules to build the entire ontology. When using RDF triplestores, this module should be always imported for first to guarantee the inter-connection and interoperability across the various modules and their data.

## Remarks:
* When using **Protégé**, if direct or indirect imports fail, it is sufficient to import manually the (not-imported) modules.
