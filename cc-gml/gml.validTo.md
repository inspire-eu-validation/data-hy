# gml.validTo

**Version**: 0.1

**Purpose**: Verify that all validTo values are from the allowed range.

**Prerequisites**

* [gml.schema-valid-1](gml.schema-valid-1.md)

**Test method**

* For each [feature](#feature) verify that either
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
feature <a name="feature"></a>   | //schema-element(gml:AbstractFeature)
validFrom <a name="validFrom"></a>   | //schema-element(gml:AbstractFeature)/\*[local-name()='validFrom']
validTo <a name="validTo"></a>   | //schema-element(gml:AbstractFeature)/\*[local-name()='validTo']
