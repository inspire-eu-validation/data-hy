# versions

**Version**: 0.1

**Purpose**: Verify that the information about a spatial object is consistent over time.

**Prerequisites**

* [gml.schema-valid-1](gml.schema-valid-1.md)

**Test method**

* Verify that identifiers are persistent for a spatial object, i.e. inspect the documentation of the spatial data set and verify that rules for identifiers are specified in a way that the identifiers (namespace and localId) do not change during the life-cycle of a spatial object. If older versions of the data set are available compare the features and verify that the namespace and localId part of the INSPIRE identifiers have not changed between the versions.
* Verify that the type of a spatial object is unchanged for different versions, i.e. inspect the documentation of the spatial data set and verify that rules for the mapping to the INSPIRE application schema are specified in a way that the spatial object type do not change during its life-cycle. If older versions of the data set are available compare the features and verify that the types of the features has not changed between the versions.
* Verify that all endLifespanVersion values are from the allowed range.
  * For all [features](#features) verify that either
    * [beginLifespanVersion](#beginLifespanVersion) or [endLifespanVersion](#endLifespanVersion) are missing or nil or
    * [endLifespanVersion](#endLifespanVersion) is not before the value of [beginLifespanVersion](#beginLifespanVersion).
  * Otherwise report [endTooEarly](#endTooEarly).

**Reference(s)**: 

* [TG DS Template](README.md#ref_TG_DS_tmpl) IR requirement Article 9 (2)
* [TG DS Template](README.md#ref_TG_DS_tmpl) IR requirement Article 10 (3)

**Test type**: Manual / Automated

## Messages

Identifier  |  Message text (parameters start with '$')
---------------------------------------------------------- | -------------------------------------------------------------------------
endTooEarly <a name="endTooEarly"/>  |  XML document '$filename', $featureType '$gmlid': The lifespan of the feature ends before it begins (property 'endLifespanVersion': '$end', property 'beginLifespanVersion': '$begin'). This is logically incorrect.

## Contextual XPath references

The namespace prefixes used as described in [README.md](README.md#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
features <a name="features"></a>   | //schema-element(hy-n3:HydroNode) \| //schema-element(hy-n3:WatercourseLink) \| //schema-element(hy-n3:WatercourseLinkSequence) \| //schema-element(hy-n3:WatercourseSeparatedCrossing) \| //schema-element(hy-n4:HydroNode) \| //schema-element(hy-n4:WatercourseLink) \| //schema-element(hy-n4:WatercourseLinkSequence) \| //schema-element(hy-n4:WatercourseSeparatedCrossing)
beginLifespanVersion <a name="beginLifespanVersion"></a>   | $features/\*[local-name()='beginLifespanVersion']
endLifespanVersion <a name="endLifespanVersion"></a>   | $features/\*[local-name()='endLifespanVersion']
