# gml.schema-valid-2

**Version**: 0.1

**Purpose**: Verify that all properties are valid according to the GML model.

**Prerequisites**

* [gml.schema-valid-1](gml.schema-valid-1.md)

**Test method**

* Inspect each property element and verify that it either carries a resolvable reference to an object (@xlink:href), contains one or more object elements as child elements or contains a non-empty text node (whitespace is trimmed before checking for empty text). Otherwise report [emptyValue](#emptyValue).

**Reference(s)**: 

* [TG DS Template](README.md#ref_TG_DS_tmpl) IR requirement Article 4 (2)

**Test type**: Automated

## Messages

Identifier  |  Message text (parameters start with '$')
---------------------------------------------------------- | -------------------------------------------------------------------------
emptyValue <a name="emptyValue"/>  |  XML document '$filename', $featureType '$gmlid': The property '$propertyName' of the feature has an empty value. While this is valid against the XML schema, this is not valid according to the GML model.

## Contextual XPath references

n/a