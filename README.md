# Islandora PREMIS

## Introduction

A Drupal 8 module that serializes PREMIS metadata generated by various Islandora modules and microsrevices. This module produces PREMIS v3 in Turtle RDF for a node by appending `/premis` to the end of the node's URL, e.g., `https://localhost/node/250/premis`.

This module is not ready for prodcution use.

Output will look like this:

```
@prefix crypHashFunc: <http://id.loc.gov/vocabulary/preservation/cryptographicHashFunctions/> .
@prefix evOutcome: <http://id.loc.gov/vocabulary/preservationevOutcome/> .
@prefix rdf:  <http://www.w3.org/1999/02/22-rdf-syntax-ns#> .
@prefix fedora:  <http://fedora.info/definitions/v4/repository#> .
@prefix ldp:  <http://www.w3.org/ns/ldp#> .
@prefix dcterms:  <http://purl.org/dc/terms/> .

<http://localhost:8080/fcrepo/rest/35/7b/f2/3b/357bf23b-0391-4128-8675-28fc080c6a8d>
        rdf:type                    fedora:Container ;
        rdf:type                    fedora:Resource ;
        rdf:type                    ldp:BasicContainer ;
        rdf:type                    <https://schema.org/DigitalDocument> ;
        rdf:type                    <http://pcdm.org/models#Object> ;
        fedora:lastModifiedBy       "bypassAdmin" ;
        <http://schema.org/dateModified>  "2019-12-09T14:41:25+00:00"^^<http://www.w3.org/2001/XMLSchema#dateTime> ;
        <http://schema.org/author>  <http://localhost:8000/user/1> ;
        <http://schema.org/sameAs>  <http://localhost:8000/node/1> ;
        <http://schema.org/dateCreated>  "2019-12-09T14:39:07+00:00"^^<http://www.w3.org/2001/XMLSchema#dateTime> ;
        dcterms:extent              "1 item" ;
        fedora:createdBy            "bypassAdmin" ;
        fedora:lastModified         "2019-12-09T14:41:26.271Z"^^<http://www.w3.org/2001/XMLSchema#dateTime> ;
        fedora:created              "2019-12-09T14:40:02.879Z"^^<http://www.w3.org/2001/XMLSchema#dateTime> ;
        dcterms:title               "A document!"@en ;
        rdf:type                    ldp:RDFSource ;
        rdf:type                    ldp:Container .

<7c6177b1-5fc9-4198-bec7-0ba7b97e9af2> a crypHashFunc:sha256 ;
        rdf:value "6933a46f55f27a62689406ea33c650b1c16d6268ee81f6c6a2a89c63aeec9d27" ;
        evType "fix" ;
        evOutcome "success" ;
<5a0f8a0c-172f-4409-a646-13279fb4c61b> a crypHashFunc:sha256 ;
        rdf:value "6933a46f55f27a62689406ea33c650b1c16d6268ee81f6c6a2a89c63aeec9d27" ;
        evType "fix" ;
        evOutcome "success" ;
<68253adc-71fb-4ddc-9edd-acb5c70d30c1> a crypHashFunc:sha256 ;
        rdf:value "6933a46f55f27a62689406ea33c650b1c16d6268ee81f6c6a2a89c63aeec9d27" ;
        evType "fix" ;
        evOutcome "success" ;
<b0fa858e-c081-4ca1-ae88-5763b4baad69> a crypHashFunc:sha256 ;
        rdf:value "6933a46f55f27a62689406ea33c650b1c16d6268ee81f6c6a2a89c63aeec9d27" ;
        evType "fix" ;
        evOutcome "success" ;
```

Note that the fixity events are added by the Islandora Riprap module, which implements Islandora PREMIS's `hook_islandora_premis_turtle_alter()` hook to add data to the PREMIS Turtle.

## Requirements

* [Islandora 8](https://github.com/Islandora/islandora)

## Installation

1. Clone this repo into your Islandora's `drupal/web/modules/contrib` directory.
1. Enable the module either under the "Admin > Extend" menu or by running `drush en -y islandora_premis`.

## Configuration

not done yet.

## Current maintainer

* [Mark Jordan](https://github.com/mjordan)

## License

[GPLv2](http://www.gnu.org/licenses/gpl-2.0.txt)
