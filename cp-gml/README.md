# Conformance class: GML application schema, Cadastral Parcels (DRAFT)

Conformance class for the GML encoding of spatial objects specified in the INSPIRE GML application schema 'Cadastral Parcels'. This conformance class examines the data set against requirements associated with the GML application schema. Both currently approved GML application schema versions (3.0 and 4.0) are tested.

This conformance class is part of the [Abstract Test Suite for the INSPIRE Data Specification on Cadastral Parcels](http://inspire.ec.europa.eu/id/ats/data-cp/3.2).

## Standardization target type

INSPIRE spatial data set encoded in GML, Cadastral Parcels

## Dependencies

### Direct dependencies

A direct dependency is another conformance class whose requirements must be met by the GML documents, too.

| Specification | Conformance class | Parameters | 
| ------------- | ----------------- | ---------- |
| [TG DS Template](#ref_TG_DS_tmpl) | [INSPIRE GML application schemas](http://inspire.ec.europa.eu/id/ats/data/3.0rc3/schemas) | n/a |

### Indirect dependencies

n/a
 
## External document references

The following abbreviations are used in the test text for referring to external documents:

Abbreviation                     | Document name
-------------------------------- | --------------------------------------------------
TG DS-CP <a name="ref_TG_DS_CP"></a>   | [INSPIRE Data Specification on Cadastral Parcels – Technical Guidelines version 3.2](http://inspire.ec.europa.eu/documents/Data_Specifications/INSPIRE_DataSpecification_CP_v3.2.pdf)
TG DS Template <a name="ref_TG_DS_tmpl"></a>   | [INSPIRE Data Specification Template version 3.0rc3](http://inspire.jrc.ec.europa.eu/documents/Data_Specifications/INSPIRE_DataSpecification_Template_v3.0rc3.pdf)

## Test Cases

| Identifier                                                        | Status   | Test case in [TG DS-PS](#ref_TG_DS_CP)  |
| ----------------------------------------------------------------- | -------- | ------------ |
| [Basic test](http://inspire.ec.europa.eu/id/ats/data-cp/3.2/cp-gml/basic)  | ready for review  | A.1.1, (A.6.1)  |

## XML namespace prefixes <a name="namespaces"></a>

The following prefixes are used to refer to the corresponding XML namespaces in all test descriptions:

Prefix         | Namespace
-------------- | -------------------------------------------------
cp            | http://inspire.ec.europa.eu/schemas/cp/4.0 or urn:x-inspire:specification:gmlas:CadastralParcels:3.0
