# gml.nilReason

**Version**: 0.1

**Purpose**: Verify that all nilReason values are from the allowed range.

**Prerequisites**

* [gml.schema-valid-1](gml.schema-valid-1.md)

**Test method**

* Inspect all [nilReason](#nilReason) values and verify that either the values from the INSPIRE registry or from GML are used. Otherwise report [incorrectReason](#incorrectReason). Valid values are:
 * 'http://inspire.ec.europa.eu/codelist/VoidReasonValue/Unknown'
 * 'http://inspire.ec.europa.eu/codelist/VoidReasonValue/Unpopulated'
 * 'http://inspire.ec.europa.eu/codelist/VoidReasonValue/Withheld'
 * 'unknown'
 * 'other:unpopulated'
 * 'withheld'

**Reference(s)**: 

* [TG DS Template](README.md#ref_TG_DS_tmpl) IR requirement Article 4 (3)

**Test type**: Automated

## Messages

Identifier  |  Message text (parameters start with '$')
---------------------------------------------------------- | -------------------------------------------------------------------------
incorrectReason <a name="incorrectReason"/>  |  XML document '$filename', $featureType '$gmlid': The property '$propertyName' of the feature has a nil value with an unexpected reason value: '$reason'. The value should either be a URI from the INSPIRE registry (see http://inspire.ec.europa.eu/codelist/VoidReasonValue) or from the pre-defined GML values ('unknown', 'other:unpopulated', or 'withheld').

## Contextual XPath references

The namespace prefixes used as described in [README.md](README.md#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
nilReason <a name="nilReason"></a>   | //@nilReason
