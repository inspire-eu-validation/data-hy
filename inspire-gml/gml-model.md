# gml-model

**Version**: 0.1

**Purpose**: Verify that the XML documents meet the requirements of the GML model that are not tested by XML schema validation alone.

**Prerequisites**

* [xml-schema](xml-schema.md)

**Test method**

* Inspect each property element and verify that it either carries a resolvable reference to an object (@xlink:href), contains one or more object elements as child elements or contains a non-empty text node (whitespace is trimmed before checking for empty text). Otherwise report [emptyValue](#emptyValue).
* Inspect each XML element that represents a feature property and that has a [nilReason](#nilReason) XML attribute. Verify that xsi:nil='true' is present in the property element, i.e. a reason is only provided in properties that are void / nil. Otherwise report [nilMissing](#nilMissing).
* Inspect all [nilReason](#nilReason) values and verify that either the values from the INSPIRE registry or the pre-defined values from the GML standard are used. Otherwise report [incorrectReason](#incorrectReason). Valid values are:
 * 'http://inspire.ec.europa.eu/codelist/VoidReasonValue/Unknown'
 * 'http://inspire.ec.europa.eu/codelist/VoidReasonValue/Unpopulated'
 * 'http://inspire.ec.europa.eu/codelist/VoidReasonValue/Withheld'
 * 'unknown'
 * 'other:unpopulated'
 * 'withheld'

**Reference(s)**: 

* [TG DS Template](README.md#ref_TG_DS_tmpl) IR requirement Article 4 (2)
* [TG DS Template](README.md#ref_TG_DS_tmpl) IR requirement Article 4 (3)

**Test type**: Automated

## Messages

Identifier  |  Message text (parameters start with '$')
---------------------------------------------------------- | -------------------------------------------------------------------------
emptyValue <a name="emptyValue"/>  |  XML document '$filename', $featureType '$gmlid': The following properties of the feature have an empty value: $propertyNames. While this is valid against the XML schema, this is not valid according to the GML model. Please correct the process that generates the GML documents. 
nilMissing <a name="nilMissing"/>  |  XML document '$filename', $featureType '$gmlid': The following properties of the feature have a nilReason attribute, but xsi:nil is not set to 'true': $propertyNames. This is an error in the GML encoding. Please correct the process that generates the GML documents. Typically it was forgotten to add xsi:nil='true' to the property element.
incorrectReason <a name="incorrectReason"/>  |  XML document '$filename', $featureType '$gmlid': The following properties of the feature have a nil value with an unexpected reason value: $propertyNamesWithNilReasonValues. The value should either be a URI from the INSPIRE registry (see http://inspire.ec.europa.eu/codelist/VoidReasonValue) or from the pre-defined GML values ('unknown', 'other:unpopulated', or 'withheld'). This is an error in the INSPIRE GML encoding and an error in the process that writes the INSPIRE GML documents.

## Contextual XPath references

The namespace prefixes used as described in [README.md](README.md#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
nilReason <a name="nilReason"></a>   | //@nilReason
