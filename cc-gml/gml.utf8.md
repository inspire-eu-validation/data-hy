# gml-utf8

**Version**: 0.1

**Purpose**: This test ensures that all linguistic texts can be encoded consistently and in any language – which in turn simplifies processing of data. The use of UTF-8 also aligns with common practice and is the default character encoding for XML documents.

**Test method**

* Inspect each XML document. If an XML declaration exists, verify that the encoding attribute has the value "UTF-8" or that the attribute is missing. Otherwise report error [notUTF8](#notUTF8).

**Reference(s)**: 

* [D2.7](README.md#ref_D2_7) requirement 12

**Test type**: Automated

## Messages

Identifier  |  Message text (parameters start with '$')
---------------------------------------------------------- | -------------------------------------------------------------------------
notUTF8 <a name="notUTF8"/>  |  XML document '$filename': UTF-8 encoding expected. The XML declaration of the document states that '$encoding' is used as the character encoding.

## Contextual XPath references

n/a