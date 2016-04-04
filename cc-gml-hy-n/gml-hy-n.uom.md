# gml-hy-n.uom

**Version**: 0.1

**Purpose**: Verify that measurements use an allowed unit.

**Prerequisites**

* [gml-hy-n.basic-test](gml-hy-n.basic-test.md)

**Test method**

* In the [features](#features), check all [unit of measurement](#uom) values. Verify that all values of the attribute @uom to be one of the following. Otherwise report [unknownUoM](#unknownUoM).
 * TODO: Compile list of units and allow the UCUM representations and OGC or INSPIRE registry URIs, where available

**Reference(s)**: 

* [TG DS Template](README.md#ref_TG_DS_tmpl) IR requirement Article 12 (2)

**Test type**: Automated

## Messages

Identifier  |  Message text (parameters start with '$')
---------------------------------------------------------- | -------------------------------------------------------------------------
unknownUoM <a name="unknownUoM"/>  |  XML document '$filename', $featureType '$gmlid': A measurement value has an unexpected unit '$uom'. The allowed values are ... TODO: add link.

## Contextual XPath references

The namespace prefixes used as described in [README.md](README.md#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
features <a name="features"></a>   | //schema-element(hy-n:HydroNode) \| //schema-element(hy-n:WatercourseLink) \| //schema-element(hy-n:WatercourseLinkSequence) \| //schema-element(hy-n:WatercourseSeparatedCrossing)
unit of measurement <a name="uom"></a>   | $features//@uom