# gml-hy-n.code-list-values

**Version**: 0.1

**Purpose**: Verify that code list values are resolvable http URIs. Where only values from the INSPIRE registry are allowed (no extensions), check this, too.

**Prerequisites**

* [gml-hy-n.basic-test](gml-hy-n.basic-test.md)

**Test method**

* For each code list value, verify that the values comply with the definitions and include the values set out in Annex II of the regulation. Otherwise report [disallowedCodeListValue](#disallowedCodeListValue).
 * TODO: compile list of feature attributes with code list values and the allowed values for each feature type. 
* Check that each value is a http URI that resolves. Otherwise report [linkDoesNotResolve](#linkDoesNotResolve).

**Reference(s)**: 

* [TG DS Template](README.md#ref_TG_DS_tmpl) IR requirement Article 4 (3)
* [TG DS Template](README.md#ref_TG_DS_tmpl) IR requirement Article 6 (1)
* INSPIRE application schema in UML

**Test type**: Automated

**Notes**

We probably need to be split this into different tests for the different types of code lists (e.g. extensible or not).

## Messages

Identifier  |  Message text (parameters start with '$')
---------------------------------------------------------- | -------------------------------------------------------------------------
disallowedCodeListValue <a name="disallowedCodeListValue"/>  |  XML document '$filename', $featureType '$gmlid': The property '$propertyName' has a value '$value' that is not one of the allowed values. 

## Contextual XPath references

The namespace prefixes used as described in [README.md](README.md#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
features <a name="features"></a>   | //schema-element(hy-n:HydroNode) \| //schema-element(hy-n:WatercourseLink) \| //schema-element(hy-n:WatercourseLinkSequence) \| //schema-element(hy-n:WatercourseSeparatedCrossing)
