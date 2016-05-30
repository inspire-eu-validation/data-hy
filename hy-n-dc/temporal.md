# temporal

**Version**: 0.1

**Purpose**: Verify that the temporal validity of the real-world entity is consistent. Note: The test case can be removed for this application schema as no feature has validTo/validFrom.

**Prerequisites**

n/a

**Test method**

* For all [features](#features) verify that either
 * [validFrom](#validFrom) or [validTo](#validTo) are missing or nil or
 * [validTo](#validTo) is not before the value of [validFrom](#validFrom).
* Otherwise report [endTooEarly](#endTooEarly).

**Reference(s)**: 

* [TG DS Template](README.md#ref_TG_DS_tmpl) IR requirement Article 10 (3)

**Test type**: Automated

## Messages

Identifier  |  Message text (parameters start with '$')
---------------------------------------------------------- | -------------------------------------------------------------------------
endTooEarly <a name="endTooEarly"/>  |  XML document '$filename', $featureType '$gmlid': The validity of the real-world entity ends before it begins (property 'validTo': '$end', property 'validFrom': '$begin'). This is logically incorrect.

## Contextual XPath references

The namespace prefixes used as described in [README.md](README.md#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
features <a name="features"></a>   | //schema-element(hy-n3:HydroNode) \| //schema-element(hy-n3:WatercourseLink) \| //schema-element(hy-n3:WatercourseLinkSequence) \| //schema-element(hy-n3:WatercourseSeparatedCrossing) \| //schema-element(hy-n4:HydroNode) \| //schema-element(hy-n4:WatercourseLink) \| //schema-element(hy-n4:WatercourseLinkSequence) \| //schema-element(hy-n4:WatercourseSeparatedCrossing)
validFrom <a name="validFrom"></a>   | $features/\*[local-name()='validFrom']
validTo <a name="validTo"></a>   | $features/\*[local-name()='validTo']
