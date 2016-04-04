# gml-hy-n.crs

**Version**: 0.1

**Purpose**: Verify that the features are Simple Features, i.e. their geometries meet the requirements of the Simple Features standard.

**Prerequisites**

* [gml-hy-n.basic-test](gml-hy-n.basic-test.md)

**Test method**

* Verify that all [references to coordinate reference systems](#srsName1) in the features use one of the http URIs from the third column of table 2. Otherwise report [unknownCRS1](#unknownCRS1).
 * TODO: Include list here
* Verify that all [references to coordinate reference systems](#srsName2) in the bounding box of the feature collection use one of the http URIs from the third column of table 2. Otherwise report [unknownCRS2](#unknownCRS2).
 * TODO: Include list here

Additional values will be added to the list for regions outside of continental Europe, if nominated by a Member State and available in a CRS register with a persistent http URI.

**Reference(s)**: 

* [TG DS Template](README.md#ref_TG_DS_tmpl) IR requirement Section 1.2
* [TG DS Template](README.md#ref_TG_DS_tmpl) IR requirement Section 1.3
* [TG DS Template](README.md#ref_TG_DS_tmpl) IR requirement Section 1.5 (1)
* [TG DS Template](README.md#ref_TG_DS_tmpl) IR requirement Section 1.5 (2)
* [TG DS Template](README.md#ref_TG_DS_tmpl) TG requirement 2

**Test type**: Automated

## Messages

Identifier  |  Message text (parameters start with '$')
---------------------------------------------------------- | -------------------------------------------------------------------------
unknownCRS1 <a name="unknownCRS1"/>  |  XML document '$filename', $featureType '$gmlid': A geometry uses an unexpected coordinate reference system '$crs'. Please refer to table 2 of the data specification for the list of expected coordinate reference systems.
unknownCRS2 <a name="unknownCRS2"/>  |  XML document '$filename': The default coordinate reference system stated in the bounding box of the feature collection has an unexpected value '$crs'. Please refer to table 2 of the data specification for the list of expected coordinate reference systems.

## Contextual XPath references

The namespace prefixes used as described in [README.md](README.md#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
features <a name="features"></a>   | //schema-element(hy-n:HydroNode) \| //schema-element(hy-n:WatercourseLink) \| //schema-element(hy-n:WatercourseLinkSequence) \| //schema-element(hy-n:WatercourseSeparatedCrossing)
srsName1 <a name="srsName1"></a>   | $features//@srsName
srsName2 <a name="srsName2"></a>   | TODO
