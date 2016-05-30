# Conformance class "INSPIRE GML encoding rule 3.3"

Conformance class for the GML encoding of spatial objects specified in the INSPIRE GML application schemas. This Abstract Test Suite examines GML documents against the requirements for the GML encoding for spatial data sets in INSPIRE. This only covers application-schema-independent, generic requirements. Requirements related to specific application schemas are part of conformance classes with a dependency on this conformance class. 

*Note*: This conformance class is under development, none of the tests have an official INSPIRE MIG approval.

*Note*: This conformance class is only temporary in this Abstract Test Suite and belongs to its own Abstract Test Suite for the 'Guidelines for the encoding of spatial data' document.

**Standardization target**: INSPIRE GML documents (spatial data sets encoded in GML)

## External document references

The following abbreviations are used in the test text for referring to external documents:

Abbreviation                     | Document name
-------------------------------- | --------------------------------------------------
INSPIRE <a name="ref_INSPIRE"></a> | [Directive 2007/2/EC of the European Parliament and of the Council of 14 March 2007 establishing an Infrastructure for Spatial Information in the European Community (INSPIRE)](http://eur-lex.europa.eu/legal-content/EN/TXT/PDF/?uri=CELEX:32007L0002&from=EN)
D2.7 <a name="ref_D2_7"></a>   | [INSPIRE Guidelines for the encoding of spatial data version 3.3](http://inspire.jrc.ec.europa.eu/documents/Data_Specifications/D2.7_v3.3.pdf)
TG DS Template <a name="ref_TG_DS_tmpl"></a>   | [INSPIRE Data Specification Template version 3.0rc3](http://inspire.jrc.ec.europa.eu/documents/Data_Specifications/INSPIRE_DataSpecification_Template_v3.0rc3.pdf)
IR ISDSS <a name="ref_IR_ISDSS"></a>   | [COMMISSION REGULATION (EU) No 1089/2010 of 23 November 2010 implementing Directive 2007/2/EC of the European Parliament and of the Council as regards interoperability of spatial data sets and services](http://eur-lex.europa.eu/legal-content/EN/TXT/PDF/?uri=OJ:L:2010:323:FULL&from=EN)
IR ISDSS Amd 1 <a name="ref_IR_ISDSS_Amd1"></a>   | [COMMISSION REGULATION (EU) No 102/2011 of 4 February 2011 amending Regulation (EU) No 1089/2010 implementing Directive 2007/2/EC of the European Parliament and of the Council as regards interoperability of spatial data sets and services](http://eur-lex.europa.eu/legal-content/EN/TXT/PDF/?uri=CELEX:32011R0102&from=EN)
IR ISDSS Amd 2 <a name="ref_IR_ISDSS_Amd2"></a>   | [COMMISSION REGULATION (EU) No 1253/2013 of 21 October 2013 amending Regulation (EU) No 1089/2010 implementing Directive 2007/2/EC as regards interoperability of spatial data sets and services](http://eur-lex.europa.eu/LexUriServ/LexUriServ.do?uri=OJ:L:2013:331:0001:0267:EN:PDF)
GML 3.2 <a name="ref_GML32"/>  | [Geography Markup Language version 3.2.1, OGC document 07-036, same as ISO 19136:2007](http://portal.opengeospatial.org/files/?artifact_id=20509) 

## Test Cases

| Identifier                                                        | Status   | Test case in current ATS  |
| ----------------------------------------------------------------- | -------- | ------------ |
| [basic](basic.md)  | Draft  | (A.6.1), A.9.5  |
| [char-encoding](char-encoding.md)  | Draft  | (A.6.1), A.9.5  |
| [xml-schema](xml-schema.md)  | Draft  | A.1.1, A.1.2, A.1.3, A.1.4, A.1.5, A.3.2, (A.6.1), A.8.1, A.9.5  |
| [gml-model](gml-model.md)  | Draft  | A.1.3, (A.6.1), A.9.5  |

## XML namespace prefixes <a name="namespaces"></a>

The following prefixes are used to refer to the corresponding XML namespaces in all test descriptions:

Prefix         | Namespace
-------------- | -------------------------------------------------
base           | http://inspire.ec.europa.eu/schemas/base/3.3
gml            | http://www.opengis.net/gml/3.2
wfs            | http://www.opengis.net/wfs/2.0
xsi            | http://www.w3.org/2001/XMLSchema-instance
xlink          | http://www.w3.org/1999/xlink
xml            | http://www.w3.org/XML/1998/namespace