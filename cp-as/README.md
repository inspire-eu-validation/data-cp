# Conformance class: Application schema, Cadastral Parcels (DRAFT)

Conformance class for the requirements associated with the application schema. 

To be able to test this conformance class, the encoding of the data set must be known, i.e. this is a parameterized conformance class. The XPath expressions used in this test suite assume that the GML encoding is used. If used with the GML encoding this conformance class has an indirect dependency to the conformance class "INSPIRE GML application schemas".

This conformance class is part of the [Abstract Test Suite for the INSPIRE Data Specification on Cadastral Parcels](http://inspire.ec.europa.eu/id/ats/data-cp/3.1).

## Standardization target type

INSPIRE spatial data set

## Dependencies

### Direct dependencies

none

### Indirect dependencies

An indirect dependency is another conformance class whose requirements must be met by a related resource.

| Specification | Conformance class | Related resource | Parameters |
| ------------- | ----------------- | ---------------- | ---------- |
| [TG DS_tmpl](http://inspire.ec.europa.eu/id/ats/data/3.0rc3/reference-systems/README#ref_TG_DS_tmpl) | [INSPIRE GML application schemas](http://inspire.ec.europa.eu/id/ats/data/3.0rc3/schemas) | INSPIRE spatial data set encoded in GML | n/a |
 
## Feature types <a name="feature-types"></a>

The instantiable feature types are:

* BasicPropertyUnit
* CadastralBoundary
* CadastralParcel
* CadastralZoning

*Note*: When "features" or "spatial objects" are mentioned in the test cases, this refers only to instances of feature types of this application schema, not to any types specified in any other application schema.

## External document references

The following abbreviations are used in the test text for referring to external documents:

Abbreviation                     | Document name
-------------------------------- | --------------------------------------------------
TG DS-CP <a name="ref_TG_DS_HY"></a>   | [INSPIRE Data Specification on Cadastral Parcels – Technical Guidelines version 3.1](http://inspire.ec.europa.eu/documents/Data_Specifications/INSPIRE_DataSpecification_CP_v3.1.pdf)
TG DS Template <a name="ref_TG_DS_tmpl"></a>   | [INSPIRE Data Specification Template version 3.0rc3](http://inspire.jrc.ec.europa.eu/documents/Data_Specifications/INSPIRE_DataSpecification_Template_v3.0rc3.pdf)

## Test Cases

| Identifier                                                        | Status   | Test case in [TG DS-HY](#ref_TG_DS_HY)  |
| ----------------------------------------------------------------- | -------- | ------------ |
| [Cadastral boundaries](http://inspire.ec.europa.eu/id/ats/data-hy/3.1/hy-n-as/cadastralBoundaries)  | Ready for review  | A.1.8  |
| [Geometry representation](http://inspire.ec.europa.eu/id/ats/data-hy/3.1/hy-n-as/geometryRepresentation)  | Open issue  | A.1.7  |
| [Modelling of object references](http://inspire.ec.europa.eu/id/ats/data-hy/3.1/hy-n-as/mor)  | Ready for review  | A.1.9  |

## XML namespace prefixes <a name="namespaces"></a>

The following prefixes are used to refer to the corresponding XML namespaces in all test descriptions:

Prefix         | Namespace
-------------- | -------------------------------------------------
cp            | http://inspire.ec.europa.eu/schemas/cp/4.0 or urn:x-inspire:specification:gmlas:CadastralParcels:3.0
cp3            | urn:x-inspire:specification:gmlas:CadastralParcels:3.0
gml            | http://www.opengis.net/gml/3.2
wfs            | http://www.opengis.net/wfs/2.0
xsi            | http://www.w3.org/2001/XMLSchema-instance
xlink          | http://www.w3.org/1999/xlink
xml            | http://www.w3.org/XML/1998/namespace
