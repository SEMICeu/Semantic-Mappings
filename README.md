# Semantic-Mappings

This repository contains all the mappings created as outcome of the alignment process of the SEMIC data specifications with other specifications such as Schema.org.

The mappings are organized for each vocabulary and aligned specifications, so for example inside Core Business folder the reader can find multiples ones, one for each a specification, such as Schema.org

The mappings are currently provided as a spreadsheet, so they can be consulted as a tabular format, and as RDF, generated with https://skos-play.sparna.fr/play/convert

The spreadsheet follows a data model which is partially based on the [Alignment Format](https://moex.gitlabpages.inria.fr/alignapi/format.html) and partially on [SSSOM](https://mapping-commons.github.io/sssom/Mapping/), making it compatible with tools using the Alignment Format, such as [VocBench](https://vocbench.uniroma2.it/) or [Silk Framework](http://silkframework.org/).

The mappings defined:
 * are 1:1 with the closest classes and properties with other specification
 * have direction from SEMIC data specifications (source) to other specifications (target)
 * make uses of RDFS (subClassOf/subPropertyOf) and OWL (equivalentClass/equivalentProperty) relations

In this way direct mapping relations could be extracted and used to perform automatic convertions (e.g. via SPARQL queries) from SEMIC data specification to other specifications. In addition, RDFS and OWL relations could be used by graph databases (such as [Virtuoso](https://docs.openlinksw.com/virtuoso/rdfsparqlruleintro/), [Jena](https://jena.apache.org/documentation/inference/) or [GraphDB](https://graphdb.ontotext.com/documentation/10.0/reasoning.html#predefined-rulesets)) or reasoners to generate new inferred triples.

# Process

The overall process is semi-automatic and it depends on 3 types of mappings: direct, indirect and mappings coming out of the matching process:

 * existing and old direct mappings have been evaluated and updated
 * indirect mappings are automatic extracted from Wikidata and DBpedia and evaluated
 * The matching process consisted of using Silk Framework which compares:
   * labels of the concepts of source and target ontologies
   * synonyms of Core Vocabularies concepts with the labels of the concepts oftarget ontology; synonyms have been automatically extrated from different services (API such as [Datamuse](https://www.datamuse.com/api/) and [Altervista](https://thesaurus.altervista.org/)) and RDF files ([Wordnet](https://wordnet-rdf.princeton.edu/license), [Wiktionary](http://kaiko.getalp.org/about-dbnary/download/), [Unesco](https://vocabularies.unesco.org/browser/thesaurus/en/), [LCSH](https://id.loc.gov/download/), [STW](https://zbw.eu/stw/version/latest/download/about.en.html), [Eurovoc](https://op.europa.eu/en/web/eu-vocabularies/dataset/-/resource?uri=http://publications.europa.eu/resource/dataset/eurovoc), [FIBO](https://github.com/edmcouncil/fibo), [LOV](https://lov.linkeddata.es/dataset/lov/sparql))

The mappings of the matching process are then imported into the spreadsheet, where manual refinement is performed considering the analysis done on direct and indirect mapping.
