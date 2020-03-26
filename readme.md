# Modularization of CIDOC CRM

This repository contains an experimental library of OWL ontologies based on the modularization of the **Erlangen release** (https://github.com/erlangen-crm/ecrm) of **CIDOC CRM** (v.6.2.1) (http://www.cidoc-crm.org/releases_table).

All the ontologies are still in the testing phase.

Stay tuned for updates.



## Repository overview

* **cidoc-whole.owl**: it imports all ontology modules, i.e., it builds the entire ontology. When using RDF triplestores, this module should be always imported for first, since it guarantees the inter-connection and interoperability across the various modules and their data.  

* **temporal-whole-module.owl**: it imports all ontology modules about temporal entities.

* **persistent-whole-module.owl**: it imports all ontology modules about persistent items.

## Remarks:
* When using **Protégé**, if direct or indirect imports fail, it is sufficient to import manually the (not-imported) modules.
