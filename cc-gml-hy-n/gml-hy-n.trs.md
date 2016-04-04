# gml-hy-n.trs

**Version**: 0.1

**Purpose**: Verify that the temporal information uses an allowed temporal reference system.

**Prerequisites**

* [gml-hy-n.basic-test](gml-hy-n.basic-test.md)

**Test method**

* In the [features](#features), check all [temporal reference system](#frame) values. Verify that only "http://www.opengis.net/def/trs/ISO-8601/" is used as a value. Otherwise report [unknownTRS](#unknownTRS).

**Reference(s)**: 

* [TG DS Template](README.md#ref_TG_DS_tmpl) IR requirement Article 11 (1)

**Test type**: Automated

*Notes*

All values in the XML Schema date/time types is automatically in the required reference system.

This test case may be removed for this application schema as no TM objects are used in the schema.

## Messages

Identifier  |  Message text (parameters start with '$')
---------------------------------------------------------- | -------------------------------------------------------------------------
unknownTRS <a name="unknownTRS"/>  |  XML document '$filename', $featureType '$gmlid': A temporal geometry uses an unexpected coordinate reference system '$trs'. Only 'http://www.opengis.net/def/trs/ISO-8601/' is allowed.

## Contextual XPath references

The namespace prefixes used as described in [README.md](README.md#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
features <a name="features"></a>   | //schema-element(hy-n:HydroNode) \| //schema-element(hy-n:WatercourseLink) \| //schema-element(hy-n:WatercourseLinkSequence) \| //schema-element(hy-n:WatercourseSeparatedCrossing)
frame <a name="frame"></a>   | $features//gml:TimeInstance/@frame \| $features//gml:TimeInstance/gml:timePosition/@frame \| $features//gml:TimePeriod/@frame \| $features//gml:TimePeriod/gml:beginPosition/@frame \| $features//gml:TimePeriod/gml:endPosition/@frame