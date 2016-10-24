# Basic test

**Version**: 1

**Purpose**: Verify that the spatial data set contains at least one CadastralParcel feature.

**Prerequisites**

**Test method**

* Check that the set of [features](#features) in the spatial data set is not empty. Otherwise report [noCadastralParcel](#noCadastralParcel)

**Reference(s)**: 

* [TG DS-PS](http://inspire.ec.europa.eu/id/ats/data-cp/3.2/cp-gml/README#ref_TG_DS_CP) IR Requirement Annex II, Section 6.1

**Test type**: Automated

**Notes**


## Messages

Identifier  |  Message text (parameters start with '$')
----------- | -------------------------------------------------------------------------
noCadastralParcel <a name="noCadastralParcel"/>  |  	The XML documents representing the spatial data set do not contain a feature of CadastralParcel. If you have expected to find CadastralParcel spatial objects in the data set, please consult the statistics information to see the spatial object types that have been found.

## Contextual XPath references

The namespace prefixes used as described in [README.md](http://inspire.ec.europa.eu/id/ats/data-ps/3.2/cp-gml/README#namespaces).

Abbreviation                                          |  XPath expression
----------------------------------------------------- | ------------------------------------------------------------------
features <a name="features"></a>   |  //schema-element(cp:CadastralParcel)