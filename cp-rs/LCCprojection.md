# Lambert Conformal Conic projection

**Version**: 1

**Purpose**: Verify whether, if data related to the spatial data theme Cadastral Parcels are made available in plane coordinates using the Lambert Conformal Conic projection, they are also made available in at least one other of the coordinate reference systems specified in sections 1.3.1, 1.3.2 and 1.3.3.

**Prerequisites**

**Test method**

* Verify that data related to the spatial data theme Cadastral Parcels made available in plane coordinates using the Lambert Conformal Conic projection, i.e. the reference to the coordinate reference system in the features ([srsName1](#srsName1)) uses the [Lambert Conformal Conic projection crsuri](#crsuriLCC), are also available in at least one other of the coordinate reference systems specified in sections 1.3.1, 1.3.2 and 1.3.3, i.e. one of the [crsuris](#crsuris) listed in TG requirement 2
* Verify that if there is a reference to the Lambert Conformal Conic projection in the bounding box of the feature collection ([srsName2](#srsName2)) by using the [Lambert Conformal Conic projection crsuri](#crsuriLCC), there is also a reference to (at least) one other of the coordinate reference systems specified in sections 1.3.1, 1.3.2 and 1.3.3, i.e. one of the [crsuris](#crsuris) listed in TG requirement 2

The Lambert Conformal Conic projection identifier:
* http://www.opengis.net/def/crs/EPSG/0/3034

The list of other coordinate reference system identifiers approved for use in INSPIRE is available in the following table: https://github.com/INSPIRE-MIF/helpdesk/blob/main/crs.md


**Reference(s)**: 

* [TG DS Template](http://inspire.ec.europa.eu/id/ats/data-cp/3.1/cp-rs/README#ref_TG_CP_tmpl) IR requirement Section 6.3.3
* [TG DS Template](http://inspire.ec.europa.eu/id/ats/data-cp/3.1/cp-rs/README#ref_TG_CP_tmpl) IR requirement Section 1.3
* [TG DS Template](http://inspire.ec.europa.eu/id/ats/data/3.0rc3/reference-systems/README#ref_TG_DS_tmpl) TG requirement 2

**Test type**: Automated/Manual

**Notes**

## Messages

Identifier  |  Message text (parameters start with '$')
---------------------------------------------------------- | -------------------------------------------------------------------------

## Contextual XPath references

The namespace prefixes used as described in [README.md](http://inspire.ec.europa.eu/id/ats/data-hy/3.1/hy-rs/README#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
srsName1 <a name="srsName1"></a>   | $features[.//@srsName[not(. = $crsuris)]]
srsName2 <a name="srsName2"></a>   | //wfs:boundedBy/\*/@srsName[not(. = $crsuris)] or //gml:boundedBy/\*/@srsName[not(. = $crsuris)]]
LCC crsuri <a name="crsuriLCC"></a> |('http://www.opengis.net/def/crs/EPSG/0/3034')
crsuris <a name="crsuris"></a>     | All the relevant HTTP URI identifiers are available in the following table: https://github.com/INSPIRE-MIF/helpdesk/blob/main/crs.md
