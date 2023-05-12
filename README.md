# Semantic-Mappings

This repository contains all the mappings created as outcome of the alignment process of the SEMIC data specifications with other specifications such as Schema.org.

Mapping are organized for each vocabulary and aligned specifications, so for example inside Core Business folder the reader can find multiples ones, one for each a specification, such as Schema.org

Mappings are currently provided as a spreadsheet, so they can be consulted as a tabular format, and as RDF, generated with https://skos-play.sparna.fr/play/convert

The spreadsheet follows a data model which is partially based on the [Alignment Format](https://moex.gitlabpages.inria.fr/alignapi/format.html) and partially on [SSSOM](https://mapping-commons.github.io/sssom/Mapping/), making it compatible with tools using the Alignment Format, such as [VocBench](https://vocbench.uniroma2.it/) or [Silk Framework](http://silkframework.org/).

The mappings defined:
 * are 1:1 with the closest classes and properties with other specification
 * have direction from SEMIC data specifications to other specifications
 * make uses of RDFS (subClassOf/subPropertyOf) and OWL (equivalentClass/equivalentProperty) axioms
 
In this way direct mapping relations could be extracted and used to perform automatic convertions (e.g. via SPARQL queries) from SEMIC data specification to other specifications.


