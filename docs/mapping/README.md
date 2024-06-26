# SSSOM mapping from PROV to Workflow Run Crate

* [PROV mapping to Workflow Run Crate](prov-mapping.tsv) (SSSOM TSV)
* [PROV mapping to Workflow Run Crate](prov-mapping.yml) (SSSOM metadata)
* [PROV mapping to Workflow Run Crate](prov-mapping-w-metadata.tsv) (SSSOM TSV with metadata)
* [PROV to Workflow Run Crate](prov-mapping.ttl) (SKOS and SSSOM OWL axioms)
* [PROV mapping to Workflow Run Crate](prov-mapping.rdf) (SSSOM OWL axioms)
* [PROV mapping to Workflow Run Crate](prov-mapping.json) (SSSOM JSON)
* [RO-Crate w/ all mappings](https://w3id.org/ro/doi/10.5281/zenodo.10368989)

## About SSSOM

SSSOM is a way to specify semantic mappings, typically based on SKOS. 

* https://mapping-commons.github.io/sssom/spec/
* https://mapping-commons.github.io/sssom/tutorial/
* https://www.w3.org/TR/skos-primer/

SSSOM mapping ar typically edited collaboratively as tab-separated text files, which can then be converted to OWL assertions using the [SSSOM toolkit](https://mapping-commons.github.io/sssom-py/).



## Editing

Please edit [prov-mapping.tsv](prov-mapping.tsv) taking care not to break the tabular characters. You may use the _Rainbow CSV_ extension in Visual Studio Code, or a spreadsheet software. 

The metadata headers are maintained in [prov-mapping.yml](prov-mapping.yml) as well as in [ro-crate-metadata.json](../ro-crate-metadata.json).

## Validating/converting

Install the [SSSOM toolkit](https://mapping-commons.github.io/sssom-py/installation.html).

If you use Conda, you can use:

```
conda env create -f environment.yml
conda activate sssom
```

Then to generate the converted file formats `prov-mapping.rdf prov-mapping.json prov-mapping.ttl` run:

```
make
```

