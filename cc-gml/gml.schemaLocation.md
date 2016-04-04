# gml.schemaLocation

**Version**: 0.1

**Purpose**: Verify that the documents can be validated against their XML schemas.

**Prerequisites**

* [gml.root-element](gml.root-element.md)

**Test method**

* Verify for each XML document that the root element that a [schemaLocation](#) attribute is provided. Otherwise report [noSchemaLocation](#noSchemaLocation)

**Reference(s)**: 

* [TG DS Template](README.md#ref_TG_DS_tmpl) IR requirement Article 4 (2)

**Test type**: Automated

## Messages

Identifier  |  Message text (parameters start with '$')
---------------------------------------------------------- | -------------------------------------------------------------------------
noSchemaLocation <a name="noSchemaLocation"/>  |  XML document '$filename':  The root element does not have an xsi:schemaLocation attribute. The document cannot be validated.

## Contextual XPath references

The namespace prefixes used as described in [README.md](README.md#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
schemaLocation <a name="schemaLocation"></a>   | /*[@xsi:schemaLocation]