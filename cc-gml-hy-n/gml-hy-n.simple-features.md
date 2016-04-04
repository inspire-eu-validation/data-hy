# gml-hy-n.simple-features

**Version**: 0.1

**Purpose**: Verify that the features are Simple Features, i.e. their geometries meet the requirements of the Simple Features standard.

**Prerequisites**

* [gml-hy-n.basic-test](gml-hy-n.basic-test.md)

**Test method**

* Verify for each [feature geometry](#geometry) that the Simple Feature requirements are met (use geometry related tests of http://schemas.opengis.net/gmlsfProfile/2.0/gmlsfL2.sch).
 * TODO: add XPath and a specific message for each test

**Reference(s)**: 

* [TG DS Template](README.md#ref_TG_DS_tmpl) IR requirement Article 12 (1)

**Test type**: Automated

## Messages

Identifier  |  Message text (parameters start with '$')
---------------------------------------------------------- | -------------------------------------------------------------------------
xxx <a name="xxx"/>  |  XML document '$filename', $featureType '$gmlid': The geometry in property '$propertyName' is not according to the Simple Feature standard.

## Contextual XPath references

The namespace prefixes used as described in [README.md](README.md#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
features <a name="features"></a>   | //schema-element(hy-n:HydroNode) \| //schema-element(hy-n:WatercourseLink) \| //schema-element(hy-n:WatercourseLinkSequence) \| //schema-element(hy-n:WatercourseSeparatedCrossing)
geometry <a name="geometry"></a> \| $features//schema-element(gml:AbstractGeometry)