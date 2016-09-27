# Modelling of object references

**Version**: 1

**Purpose**: Verify whether all instances of the spatial object type CadastralParcel carry as a thematic identifier the attribute nationalCadastralReference. This attribute must enable users to make the link with rights, owners and other cadastral information in national cadastral registers or equivalent.

**Prerequisites**

**Test method**
Automated assertions:

* Check that all instances of the spatial object type [CadastralParcel](#CadastralParcel) have as a thematic identifier the attribute [nationalCadastralReference](#ncr).

Manual assertions:

* Check that the value of the attribute [nationalCadastralReference](#ncr) enables the users to make the link with rights, owners and other cadastral information in national cadastral registers or equivalent.

**Reference(s)**: 

* [TG DS-CP](http://inspire.ec.europa.eu/id/ats/data-cp/3.1/cp-as/README#ref_TG_DS_CP) IR requirement Section 6.3.2

**Test type**: Automated/Manual

**Notes**


## Messages

Identifier  |  Message text (parameters start with '$')
----------- | -------------------------------------------------------------------------

## Contextual XPath references

The namespace prefixes used as described in [README.md](http://inspire.ec.europa.eu/id/ats/data-hy/3.1/hy-gml/README#namespaces).

Abbreviation                                          |  XPath expression
----------------------------------------------------- | ------------------------------------------------------------------
Cadastral Parcel <a name="CadastralParcel"></a>   | //schema-element(cp:CadastralParcel)
nationalCadastralReference <a name="ncr")></a>  | //schema-element(cp:CadastralParcel)/cp:nationalCadastralReference
