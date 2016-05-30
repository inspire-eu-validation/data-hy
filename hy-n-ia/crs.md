# code-list

**Version**: 0.1

**Purpose**: Verify that referenced coordinate reference systems can be accessed.

**Prerequisites**

n/a

**Test method**

* Verify that any coordinate reference system is publicly accessible via HTTP, i.e. inspect links to coordinate reference systems. Verify that each link ([srsName1](#srsName1), [srsName2](#srsName2), [frame](#frame)) resolves to a definition of the reference system. Otherwise report [linkDoesNotResolve](#linkDoesNotResolve).

**Reference(s)**: 

* [TG DS Template](README.md#ref_TG_DS_tmpl) IR requirement Section 1.3.4
* [TG DS Template](README.md#ref_TG_DS_tmpl) IR requirement Section 1.5.1
* [TG DS Template](README.md#ref_TG_DS_tmpl) IR requirement Section 1.5.2

**Test type**: Automated

**Notes**

This assertion can be removed as the application schema does not specify any extensible code lists.

## Messages

Identifier  |  Message text (parameters start with '$')
---------------------------------------------------------- | -------------------------------------------------------------------------
linkDoesNotResolve <a name="linkDoesNotResolve"/>  |  XML document '$filename', $featureType '$gmlid': A spatial or temporal geometry uses an unexpected, unresolvable coordinate reference system with identifier '$rsid'. Every URI must be a HTTP URI in a CRS register that resolves to a definition of the reference system.

## Contextual XPath references

The namespace prefixes used as described in [README.md](README.md#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
features <a name="features"></a>   | //schema-element(hy-n3:HydroNode) \| //schema-element(hy-n3:WatercourseLink) \| //schema-element(hy-n3:WatercourseLinkSequence) \| //schema-element(hy-n3:WatercourseSeparatedCrossing) \| //schema-element(hy-n4:HydroNode) \| //schema-element(hy-n4:WatercourseLink) \| //schema-element(hy-n4:WatercourseLinkSequence) \| //schema-element(hy-n4:WatercourseSeparatedCrossing)
frame <a name="frame"></a>   | $features//gml:TimeInstance/@frame \| $features//gml:TimeInstance/gml:timePosition/@frame \| $features//gml:TimePeriod/@frame \| $features//gml:TimePeriod/gml:beginPosition/@frame \| $features//gml:TimePeriod/gml:endPosition/@frame
srsName1 <a name="srsName1"></a>   | $features[.//@srsName[not(. = $crsuris)]]
srsName2 <a name="srsName2"></a>   | //wfs:boundedBy/\*/@srsName[not(. = $crsuris)] or //gml:boundedBy/\*/@srsName[not(. = $crsuris)]]
