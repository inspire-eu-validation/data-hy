# xml-schema

**Version**: 0.1

**Purpose**: Verify that all XML documents validate against their XML schema(s).

**Prerequisites**

* [basic](basic.md)

**Test method**

* Verify for each XML document that the root element that a [schemaLocation](#) attribute is provided. Otherwise report [noSchemaLocation](#noSchemaLocation)
* Validate each document against the schema(s) specified in the xsi:schemaLocation attribute using strict XML schema validation. Otherwise report [invalidSchema](#invalidSchema).

**Reference(s)**: 

* [TG DS Template](README.md#ref_TG_DS_tmpl) IR requirement Article 3
* [TG DS Template](README.md#ref_TG_DS_tmpl) IR requirement Article 4 (2)
* [TG DS Template](README.md#ref_TG_DS_tmpl) IR requirement Article 4 (3)
* [TG DS Template](README.md#ref_TG_DS_tmpl) IR requirement Article 5 (2)
* [TG DS Template](README.md#ref_TG_DS_tmpl) IR requirement Article 5 (3)
* [TG DS Template](README.md#ref_TG_DS_tmpl) IR requirement Article 6 (5)
* [TG DS Template](README.md#ref_TG_DS_tmpl) IR requirement Article 9 (1)
* [TG DS Template](README.md#ref_TG_DS_tmpl) TG requirement 1
* [TG DS Template](README.md#ref_TG_DS_tmpl) TG requirement 6

**Test type**: Automated

## Messages

Identifier  |  Message text (parameters start with '$')
---------------------------------------------------------- | -------------------------------------------------------------------------
noSchemaLocation <a name="noSchemaLocation"/>  |  XML document '$filename':  The root element does not have an xsi:schemaLocation attribute. The document cannot be validated.
invalidSchema <a name="invalidSchema"/>  |  XML document '$filename':  The document is not valid. The XML parser has identified the following issues: $issues

## Contextual XPath references

The namespace prefixes used as described in [README.md](README.md#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
schemaLocation <a name="schemaLocation"></a>   | /*[@xsi:schemaLocation]