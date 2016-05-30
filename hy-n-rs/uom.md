# uom

**Version**: 0.1

**Purpose**: Verify that measurements use an allowed unit.

**Prerequisites**

n/a

**Test method**

* Verify that all references to a unit of measurement uses one of the approved http URIs or values from the UCUM dictionary. In the [features](#features), check all unit of measurement values ([uom](#uom)). Verify that all values of the attribute @uom to be one of the approved http URIs or values from the UCUM dictionary for the feature types of this application schema. Otherwise report [unknownUoM](#unknownUoM).

**Reference(s)**: 

* [TG DS Template](README.md#ref_TG_DS_tmpl) IR requirement Article 12 (2)

**Test type**: Automated

**Notes**:

The list of valid values still has to be compiled for this application schema. 

## Messages

Identifier  |  Message text (parameters start with '$')
---------------------------------------------------------- | -------------------------------------------------------------------------
unknownUoM <a name="unknownUoM"/>  |  XML document '$filename', $featureType '$gmlid': A measurement value has an unexpected unit '$uom'. The allowed values are ... TODO.

## Contextual XPath references

The namespace prefixes used as described in [README.md](README.md#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
features <a name="features"></a>   | //schema-element(hy-n3:HydroNode) \| //schema-element(hy-n3:WatercourseLink) \| //schema-element(hy-n3:WatercourseLinkSequence) \| //schema-element(hy-n3:WatercourseSeparatedCrossing) \| //schema-element(hy-n4:HydroNode) \| //schema-element(hy-n4:WatercourseLink) \| //schema-element(hy-n4:WatercourseLinkSequence) \| //schema-element(hy-n4:WatercourseSeparatedCrossing)
uom <a name="uom"></a>   | $features//@uom