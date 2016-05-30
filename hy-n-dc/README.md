# Conformance class "Data Consistency, Hydrography - Network 3.1"

Conformance class for the requirements related to the consistency of the data.

To be able to test this conformance class, the encoding of the data set must be known, i.e. this is a parameterized conformance class. The XPath expressions used in this test suite assume that the GML encoding is used. If used with the GML encoding this conformance class has an indirect dependency to the conformance class "GML application schema for Hydrography - Network 3.0/4.0".

*Note*: This conformance class is under development, none of the tests have an official INSPIRE MIG approval.

**URI**: http://inspire.ec.europa.eu/conformance-class/ir/hy/dc/hy-n/3.1

**Standardization target**: INSPIRE spatial data set

The instantiable feature types in the application schema are:

* HydroNode
* WatercourseLink
* WatercourseLinkSequence
* WatercourseSeparatedCrossing

*Note*: When we mention "features" in the test cases, this refers only to the features (spatial object types) of this application schema, not to any feature specified in any other application schema.

## External document references

The following abbreviations are used in the test text for referring to external documents:

Abbreviation                     | Document name
-------------------------------- | --------------------------------------------------
INSPIRE <a name="ref_INSPIRE"></a> | [Directive 2007/2/EC of the European Parliament and of the Council of 14 March 2007 establishing an Infrastructure for Spatial Information in the European Community (INSPIRE)](http://eur-lex.europa.eu/legal-content/EN/TXT/PDF/?uri=CELEX:32007L0002&from=EN)
D2.7 <a name="ref_D2_7"></a>   | [INSPIRE Guidelines for the encoding of spatial data version 3.3](http://inspire.jrc.ec.europa.eu/documents/Data_Specifications/D2.7_v3.3.pdf)
TG DS Template <a name="ref_TG_DS_tmpl"></a>   | [INSPIRE Data Specification Template version 3.0rc3](http://inspire.jrc.ec.europa.eu/documents/Data_Specifications/INSPIRE_DataSpecification_Template_v3.0rc3.pdf)
TG DS-HY <a name="ref_TG_DS_HY"></a>   | [INSPIRE Data Specification on Hydrography – Technical Guidelines version 3.1](http://inspire.ec.europa.eu/documents/Data_Specifications/INSPIRE_DataSpecification_HY_v3.1.pdf)
IR ISDSS <a name="ref_IR_ISDSS"></a>   | [COMMISSION REGULATION (EU) No 1089/2010 of 23 November 2010 implementing Directive 2007/2/EC of the European Parliament and of the Council as regards interoperability of spatial data sets and services](http://eur-lex.europa.eu/legal-content/EN/TXT/PDF/?uri=OJ:L:2010:323:FULL&from=EN)
IR ISDSS Amd 1 <a name="ref_IR_ISDSS_Amd1"></a>   | [COMMISSION REGULATION (EU) No 102/2011 of 4 February 2011 amending Regulation (EU) No 1089/2010 implementing Directive 2007/2/EC of the European Parliament and of the Council as regards interoperability of spatial data sets and services](http://eur-lex.europa.eu/legal-content/EN/TXT/PDF/?uri=CELEX:32011R0102&from=EN)
IR ISDSS Amd 2 <a name="ref_IR_ISDSS_Amd2"></a>   | [COMMISSION REGULATION (EU) No 1253/2013 of 21 October 2013 amending Regulation (EU) No 1089/2010 implementing Directive 2007/2/EC as regards interoperability of spatial data sets and services](http://eur-lex.europa.eu/LexUriServ/LexUriServ.do?uri=OJ:L:2013:331:0001:0267:EN:PDF)
GML 3.2 <a name="ref_GML32"/>  | [Geography Markup Language version 3.2.1, OGC document 07-036, same as ISO 19136:2007](http://portal.opengeospatial.org/files/?artifact_id=20509) 

## Test Cases

| Identifier                                                        | Status   | Test case in current ATS  |
| ----------------------------------------------------------------- | -------- | ------------ |
| [versions](versions.md)  | Draft  | A.3.1, A.3.2, A.3.3 |
| [temporal](temporal.md)  | Draft  | A.3.4  |
| [spatial](spatial.md)  | Draft  | A.1.7, A.3.6  |
| [thematic](thematic.md)  | Draft  | A.3.6  |
| [identifiers](identifiers.md)  | Draft  | A.3.7  |

Note: A test case seems to be missing for A.3.5 (update frequency).

## XML namespace prefixes <a name="namespaces"></a>

The following prefixes are used to refer to the corresponding XML namespaces in all test descriptions:

Prefix         | Namespace
-------------- | -------------------------------------------------
hy-n3          | http://inspire.ec.europa.eu/schemas/hy-n/3.0
hy-n4          | http://inspire.ec.europa.eu/schemas/hy-n/4.0
hy-p3          | http://inspire.ec.europa.eu/schemas/hy-p/3.0
hy-p4          | http://inspire.ec.europa.eu/schemas/hy-p/4.0
gml            | http://www.opengis.net/gml/3.2
