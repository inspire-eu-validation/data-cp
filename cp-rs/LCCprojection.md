# Lambert Conformal Conic projection

**Version**: 1

**Purpose**: Verify whether, if data related to the spatial data theme Cadastral Parcels are made available in plane coordinates using the Lambert Conformal Conic projection, they are also made available in at least one other of the coordinate reference systems specified in sections 1.3.1, 1.3.2 and 1.3.3.

**Prerequisites**

**Test method**

* Verify that data related to the spatial data theme Cadastral Parcels made available in plane coordinates using the Lambert Conformal Conic projection, i.e. the reference to the coordinate reference system in the features ([srsName1](#srsName1)) uses the [Lambert Conformal Conic projection crsuri](#crsuriLCC), are also available in at least one other of the coordinate reference systems specified in sections 1.3.1, 1.3.2 and 1.3.3, i.e. one of the [crsuris](#crsuris) listed in TG requirement 2
* Verify that if there is a reference to the Lambert Conformal Conic projection in the bounding box of the feature collection ([srsName2](#srsName2)) by using the [Lambert Conformal Conic projection crsuri](#crsuriLCC), there is also a reference to (at least) one other of the coordinate reference systems specified in sections 1.3.1, 1.3.2 and 1.3.3, i.e. one of the [crsuris](#crsuris) listed in TG requirement 2

The Lambert Conformal Conic projection identifier:
* http://www.opengis.net/def/crs/EPSG/0/3034

The list of other coordinate reference system identifiers: 
* http://www.opengis.net/def/crs/EPSG/0/4936
* http://www.opengis.net/def/crs/EPSG/0/4937
* http://www.opengis.net/def/crs/EPSG/0/4258
* http://www.opengis.net/def/crs/EPSG/0/3035
* http://www.opengis.net/def/crs/EPSG/0/3038
* http://www.opengis.net/def/crs/EPSG/0/3039
* http://www.opengis.net/def/crs/EPSG/0/3040
* http://www.opengis.net/def/crs/EPSG/0/3041
* http://www.opengis.net/def/crs/EPSG/0/3042
* http://www.opengis.net/def/crs/EPSG/0/3043
* http://www.opengis.net/def/crs/EPSG/0/3044
* http://www.opengis.net/def/crs/EPSG/0/3045
* http://www.opengis.net/def/crs/EPSG/0/3046
* http://www.opengis.net/def/crs/EPSG/0/3047
* http://www.opengis.net/def/crs/EPSG/0/3048
* http://www.opengis.net/def/crs/EPSG/0/3049
* http://www.opengis.net/def/crs/EPSG/0/3050
* http://www.opengis.net/def/crs/EPSG/0/3051
* http://www.opengis.net/def/crs/EPSG/0/5730
* http://www.opengis.net/def/crs/EPSG/0/7409

**Reference(s)**: 

* [TG DS Template](http://inspire.ec.europa.eu/id/ats/data-cp/3.1/cp-rs/README#ref_TG_CP_tmpl) IR requirement Section 6.3.3

**Test type**: Automated

**Notes**

## Messages

Identifier  |  Message text (parameters start with '$')
---------------------------------------------------------- | -------------------------------------------------------------------------

## Contextual XPath references

The namespace prefixes used as described in [README.md](http://inspire.ec.europa.eu/id/ats/data-hy/3.1/hy-rs/README#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------

