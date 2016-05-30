# temporal

**Version**: 0.1

**Purpose**: Verify that all references to temporal coordinate reference systems are using one of the http URIs approved for use in INSPIRE data sets.

**Prerequisites**

n/a

**Test method**

* Verify that all references to coordinate reference systems in the features use one of the approved http URIs, i.e. check that all references to coordinate reference systems in the [frame](#frame) XML attributes in the [features](#features) use the URI 'http://www.opengis.net/def/trs/ISO-8601/'. Otherwise report [unknownTRS](#unknownTRS). 

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
features <a name="features"></a>   | //schema-element(hy-n3:HydroNode) \| //schema-element(hy-n3:WatercourseLink) \| //schema-element(hy-n3:WatercourseLinkSequence) \| //schema-element(hy-n3:WatercourseSeparatedCrossing) \| //schema-element(hy-n4:HydroNode) \| //schema-element(hy-n4:WatercourseLink) \| //schema-element(hy-n4:WatercourseLinkSequence) \| //schema-element(hy-n4:WatercourseSeparatedCrossing)
frame <a name="frame"></a>   | $features//gml:TimeInstance/@frame \| $features//gml:TimeInstance/gml:timePosition/@frame \| $features//gml:TimePeriod/@frame \| $features//gml:TimePeriod/gml:beginPosition/@frame \| $features//gml:TimePeriod/gml:endPosition/@frame