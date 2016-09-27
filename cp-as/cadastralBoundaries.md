# Cadastral Boundaries

**Version**: 1

**Purpose**: Verify whether, if cadastral boundaries are provided, the cadastral boundaries corresponding to the outline of a cadastral parcel form closed ring(s).

**Prerequisites**

**Test method**

* Check that [cadastral boundaries](#CadastralBoundary) corresponding to the outline of a [cadastral parcel](#CadastralParcel) form closed ring (s).

**Reference(s)**: 

* [TG DS-CP](http://inspire.ec.europa.eu/id/ats/data-cp/3.1/cp-as/README#ref_TG_DS_CP) IR requirement Section 6.3.1 (1)

**Test type**: Automated

**Notes**


## Messages

Identifier  |  Message text (parameters start with '$')
----------- | -------------------------------------------------------------------------

## Contextual XPath references

The namespace prefixes used as described in [README.md](http://inspire.ec.europa.eu/id/ats/data-hy/3.1/hy-gml/README#namespaces).

Abbreviation                                          |  XPath expression
----------------------------------------------------- | ------------------------------------------------------------------
Cadastral Boundary <a name="CadastralBoundary"></a>   | //schema-element(cp:CadastralBoundary)
Cadastral parcel <a name="CadastralParcel"></a>   | //schema-element(cp:CadastralBoundary)/cp:parcel)
