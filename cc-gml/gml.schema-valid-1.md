# gml.schema-valid-1

**Version**: 0.1

**Purpose**: Verify that the documents are schema valid.

**Prerequisites**

* [gml.schemaLocation](gml.schemaLocation.md)

**Test method**

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
invalidSchema <a name="invalidSchema"/>  |  XML document '$filename':  The document is not valid. The XML parser has identified the following issues: $issues

## Contextual XPath references

n/a