# gml.endLifespanVersion

**Version**: 0.1

**Purpose**: Verify that all endLifespanVersion values are from the allowed range.

**Prerequisites**

* [gml.schema-valid-1](gml.schema-valid-1.md)

**Test method**

* For each [feature](#feature) verify that either
 * [beginLifespanVersion](#beginLifespanVersion) or [endLifespanVersion](#endLifespanVersion) are missing or nil or
 * [endLifespanVersion](#endLifespanVersion) is not before the value of [beginLifespanVersion](#beginLifespanVersion).
* Otherwise report [endTooEarly](#endTooEarly).

**Reference(s)**: 

* [TG DS Template](README.md#ref_TG_DS_tmpl) IR requirement Article 10 (3)

**Test type**: Automated

## Messages

Identifier  |  Message text (parameters start with '$')
---------------------------------------------------------- | -------------------------------------------------------------------------
endTooEarly <a name="endTooEarly"/>  |  XML document '$filename', $featureType '$gmlid': The lifespan of the feature ends before it begins (property 'endLifespanVersion': '$end', property 'beginLifespanVersion': '$begin'). This is logically incorrect.

## Contextual XPath references

The namespace prefixes used as described in [README.md](README.md#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
feature <a name="feature"></a>   | //schema-element(gml:AbstractFeature)
beginLifespanVersion <a name="beginLifespanVersion"></a>   | //schema-element(gml:AbstractFeature)/\*[local-name()='beginLifespanVersion']
endLifespanVersion <a name="endLifespanVersion"></a>   | //schema-element(gml:AbstractFeature)/\*[local-name()='endLifespanVersion']
