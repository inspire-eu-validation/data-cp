# Constraints

**Version**: 1

**Purpose**: Verify that the features provided in the dataset adhere to the constraints specified in the INSPIRE application schema.

**Prerequisites**

**Test method**

Verify that the OCL constraints listed below that are specified in the UML model of the application schema are met, i.e. validate features against the constraints. For unmet constraints report [constraintViolation](#constraintViolation). 

For constraints that require retrieving a referenced resource and the resource cannot be retrieved, report [brokenLink](#brokenLink). The test accepts the following two types of content in @xlink:href attributes: Either a "#" followed by a @gml:id in the same document or a HTTP URI.

Automated tests:

* Value of areaValue shall be given in square meters; OCL: "inv: self.areaValue.uom.uomSymbol='m2'". Verify that BasicPropertyUnit.[areaValue.uom](#uomAreaValue) and CadastralParcel.[areaValue.uom](#uomAreaValue) are given in 'm2'.
* Value of estimatedAccuracy shall be given in meters; OCL: "inv: self.estimatedAccuracy.uom.uomSymbol='m'". Verify that CadastralBoundary.[estimatedAccuracy.uom](#estimatedAccuracyUoM) and CadastralZoning.[estimatedAccuracy.uom](#estimatedAccuracyUoM) are given in 'm'.
* Type of geometry shall be GM_Surface or GM_MultiSurface; OCL "inv: geometry.oclIsKindOf(GM_Surface) or geometry.oclIsKindOf(GM_MultiSurface)". verify that CadastralParcel.[geometryType](#geometryType) is a gml:Surface or gml:MutiSurface.
* A lower level cadastral zoning shall be part of an upper level zoning. OCL: "inv: self.nationalLevel <> '1stOrder' implies self.level < self.upperLevelUnit.level". Verify that for a [CadastralZoning](#CadastralZoning) not of the [nationalLevel](#nationalLevel) 1st Order, its own level is lower than the level of the [CadastralZoning](#CadastralZoning) referenced in [upperLevelUnit](#upperLevelUnit)


**Reference(s)**: 

* [TG DS Template](http://inspire.ec.europa.eu/id/ats/data-cp/3.2/cp-as/README#ref_TG_DS_tmpl) IR requirement Article 4 (2)
* [TG DS-PS](http://inspire.ec.europa.eu/id/ats/data-cp/3.2/cp-as/README#ref_TG_DS_PS)) 5.4

**Test type**: Automated

## Messages

Identifier  |  Message text (parameters start with '$')
---------------------------------------------------------- | -------------------------------------------------------------------------
constraintViolation <a name="constraintViolation"/>  |  XML document '$filename', $featureType '$gmlid': The constraint '$constraint' is violated.
brokenLink <a name="brokenLink"/>  |  XML document '$filename', $featureType '$gmlid': The property '$propertyName' has a value '$value' that cannot be retrieved using HTTP.

## Contextual XPath references

The namespace prefixes used as described in [README.md](http://inspire.ec.europa.eu/id/ats/data-cp/3.2/cp-as/README#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
areaValue.uom <a name="uomAreaValue"></a> 	| 	//schema-element(cp:BasicPropertyUnit)/cp:areaValue/@uom/text() or //schema-element(cp:CadastralParcel)/cp:areaValue/@uom/text()
estimatedAccuracy.uom <a name="estimatedAccuracyUoM"></a> 	| //schema-element(cp:CadastralBoundary)/cp:estimatedAccuracy/@uom/text() or //schema-element(cp:CadastralZoning)/cp:estimatedAccuracy/@uom/text()
geometryType <a name="geometryType"></a> 	| 	//schema-element(cp:CadastralParcel)/cp:geometry/*
CadastralZoning  <a name="CadastralZoning"></a> 	| 	//schema-element(cp:CadastralZoning)
nationalLevel <a name="nationalLevel"></a> 	| 	//schema-element(cp:CadastralZoning)/cp:nationalLevel/@xlink:href or //schema-element(cp3:CadastralZoning)/cp3:nationalLevel/text()
upperLevelUnit <a name="upperLevelUnit"></a> 	| 	//schema-element(cp:CadastralZoning)/cp:upperLevelUnit