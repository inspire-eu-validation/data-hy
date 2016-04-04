# gml-hy-n.constraints

**Version**: 0.1

**Purpose**: Verify that the OCL constraints specified in the UML model of the application schema are met.

**Prerequisites**

* [gml-hy-n.basic-test](gml-hy-n.basic-test.md)

**Test method**

* Validate [features](#features) against the OCL constraints included in the UML model of the INSPIRE application schemas:
 * TODO: extract constraints from UML for the feature types and convert to XQuery/XPath)
* For unmet constraints report [constraintViolation](#constraintViolation)

**Reference(s)**: 

* [TG DS Template](README.md#ref_TG_DS_tmpl) IR requirement Article 4 (2)
* INSPIRE application schema in UML

**Test type**: Automated

## Messages

Identifier  |  Message text (parameters start with '$')
---------------------------------------------------------- | -------------------------------------------------------------------------
constraintViolation <a name="constraintViolation"/>  |  XML document '$filename', $featureType '$gmlid': The constraint '$constraint' is violated.

## Contextual XPath references

The namespace prefixes used as described in [README.md](README.md#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
features <a name="features"></a>   | //schema-element(hy-n:HydroNode) \| //schema-element(hy-n:WatercourseLink) \| //schema-element(hy-n:WatercourseLinkSequence) \| //schema-element(hy-n:WatercourseSeparatedCrossing)
