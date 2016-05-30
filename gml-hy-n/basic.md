# basic

**Version**: 0.1

**Purpose**: Verify that the spatial data set contains at least one Hydro - Network feature.

**Prerequisites**

n/a

**Test method**

* Check that the set of [features](#features) in the spatial data set is not empty. Otherwise report [noFeature](#noFeature)

**Reference(s)**: 

* [TG DS-HY](README.md#ref_TG_DS_HY) 5.4

**Test type**: Automated

**Notes**

There is no requirement that we could reference in the Technical Guidelines. Maybe one should be added in the future revision?

## Messages

Identifier  |  Message text (parameters start with '$')
---------------------------------------------------------- | -------------------------------------------------------------------------
noFeature <a name="noFeature"/>  |  	The XML documents representing the spatial data set do not contain a feature of any of the spatial object types in the 'Hydrography - Network' application schema. Therefore, the spatial data set cannot conform to this conformance class. If you have expected to find spatial objects from the application schema in the data set, please consult the statistics information to see the spatial object types that have been found.

## Contextual XPath references

The namespace prefixes used as described in [README.md](README.md#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
features <a name="features"></a>   | //schema-element(hy-n3:HydroNode) \| //schema-element(hy-n3:WatercourseLink) \| //schema-element(hy-n3:WatercourseLinkSequence) \| //schema-element(hy-n3:WatercourseSeparatedCrossing) \| //schema-element(hy-n4:HydroNode) \| //schema-element(hy-n4:WatercourseLink) \| //schema-element(hy-n4:WatercourseLinkSequence) \| //schema-element(hy-n4:WatercourseSeparatedCrossing)