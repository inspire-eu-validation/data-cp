# Feature references

**Version**: 1

**Purpose**: Verify that referenced features can be retrieved.

**Prerequisites**

**Test method**

* Verify that any feature reference in an association role is publicly accessible via HTTP, i.e. inspect all relevant properties. If a reference (@xlink:href) has a value that starts with "#", verify that an element with a `gml:id` attribute with the referenced identifier exists in the same document. If the reference starts with "http", verify that a HTTP GET request to the URI retrieves an XML document. Otherwise report [brokenLink](#brokenLink).

This data theme currently has the following asscoiation roles:

* BasicPropertyUnit.[administrativeUnit](#administrativeUnit) : AdministrativeUnit
* CadastralBoundary.[parcel](#parcel) : CadastralParcel
* CadastralParcel.[basicPropertyUnit](#basicPropertyUnit) : BasicPropertyUnit
* CadastralParcel.[administrativeUnit](#administrativeUnit) : AdministrativeUnit
* CadastralParcel.[zoning](#zoning) : CadastralZoning
* CadastralZoning.[upperLevelUnit](#upperLevelUnit) : CadastralZoning

**Reference(s)**: 

* [TG DS Template](http://inspire.ec.europa.eu/id/ats/data-au/3.1/au-ia/README#ref_TG_DS_tmpl) IR requirement Article 4 (2)

**Test type**: Automated

**Notes**

## Messages

Identifier  |  Message text (parameters start with '$')
---------------------------------------------------------- | -------------------------------------------------------------------------
brokenLink <a name="brokenLink"/>  |  XML document '$filename', $featureType '$gmlid': The property '$propertyName' has a value '$value' that cannot be retrieved using HTTP. Every code list value must be made available in an online registry. 

## Contextual XPath references

The namespace prefixes used as described in [README.md](http://inspire.ec.europa.eu/id/ats/data-hy/3.1/hy-ia/README#namespaces).

Abbreviation                         |  XPath expression    | Multiplicity    | Voidable
------------------------------------ | ---------------------|-----------------|-----------------------------
administrativeUnit <a name="administrativeUnit"></a> |  //schema-element(cp:BasicPropertyUnit)/cp:administrativeUnit/@xlink:href or <br> //schema-element(cp:CadastralParcel)/cp:administrativeUnit/@xlink:href | 1 <br> 0..1 | Yes <br> No
parcel <a name="parcel"></a>	| //schema-element(cp:CadastralBoundary)/cp:parcel/@xlink:href | 1..2 | Yes
basicPropertyUnit <a name="basicPropertyUnit"></a>	| //schema-element(cp:CadastralParcel)/cp:basicPropertyUnit/@xlink:href | 0..\* | Yes
zoning <a name="zoning"></a>	| //schema-element(cp:CadastralParcel)/cp:zoning/@xlink:href | 0..1 | Yes
upperLevelUnit <a name="upperLevelUnit"></a>	| //schema-element(cp:CadastralZoning)/cp:upperLevelUnit/@xlink:href | 0..1 | Yes
