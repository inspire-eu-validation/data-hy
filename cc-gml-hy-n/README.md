# Conformance Class "GML encoding of application schema 'Hydro - Network', version 4.0"

Conformance class for the GML encoding of spatial objects specified in the INSPIRE GML application schema 'Hydro - Network', version 4.0.

*Note*: This conformance class is under development, none of the tests have an official INSPIRE MIG approval.

**URI**: http://inspire.ec.europa.eu/conformance-class/tg/hy-n/3.1 

**Standardization target**: INSPIRE spatial data sets encoded in GML that include at least one feature of the INSPIRE GML application schema 'Hydro - Network'.

The instantiable feature types in the application schema are:
* hy-n:HydroNode
* hy-n:WatercourseLink
* hy-n:WatercourseLinkSequence
* hy-n:WatercourseSeparatedCrossing

*Note*: The XML Schema declarations of each feature in a non-INSPIRE namespace have to be accessed. Recursively identify the first element in an INSPIRE or GML namespace. If it is one of the above, treat these features in the tests as if they were of that INSPIRE feature type.

*Note*: When we mention "features" in the test cases, this refers only to the features of this application schema (and not to any feature specified in another INSPIRE application schema).

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
| [gml-hy-n.attribute-consistency](gml-hy-n.attribute-consistency.md)  | Draft  | A.3.6 |
| [gml-hy-n.basic-test](gml-hy-n.basic-test.md)  | Draft  | n/a |
| [gml-hy-n.code-list-values](gml-hy-n.code-list-values.md)  | Draft  | A.1.3, A.6.1  |
| [gml-hy-n.consistency-at-borders](gml-hy-n.consistency-at-borders.md)  | Draft  | A.3.6 |
| [gml-hy-n.constraints](gml-hy-n.constraints.md)  | Draft  | A.1.6  |
| [gml-hy-n.crs](gml-hy-n.crs.md)  | Draft  | A.2.1, A.2.2, A.6.2, A.6.3, A.9.1  |
| [gml-hy-n.delineationKnown](gml-hy-n.delineationKnown.md)  | Draft  | A.1.9  |
| [gml-hy-n.geometry-consistency](gml-hy-n.geometry-consistency.md)  | Draft  | A.1.7  |
| [gml-hy-n.identifier-consistency](gml-hy-n.identifier-consistency.md)  | Draft  | A.3.7 |
| [gml-hy-n.identifier-source](gml-hy-n.identifier-source.md)  | Draft  | A.3.7  |
| [gml-hy-n.linear-referencing](gml-hy-n.linear-referencing.md)  | Draft  | A.1.8 |
| [gml-hy-n.link-centrelines](gml-hy-n.link-centrelines.md)  | Draft  | A.1.10  |
| [gml-hy-n.link-intersections](gml-hy-n.link-intersections.md)  | Draft  | A.1.7 |
| [gml-hy-n.multiple-resolutions](gml-hy-n.multiple-resolutions.md)  | Draft  | A.1.7 |
| [gml-hy-n.network-connectivity-1](gml-hy-n.network-connectivity-1.md)  | Draft  | A.1.11  |
| [gml-hy-n.network-connectivity-2](gml-hy-n.network-connectivity-2.md)  | Draft  | A.1.11  |
| [gml-hy-n.network-connectivity-3](gml-hy-n.network-connectivity-3.md)  | Draft  | A.1.11  |
| [gml-hy-n.network-connectivity-4](gml-hy-n.network-connectivity-4.md)  | Draft  | A.1.11  |
| [gml-hy-n.no-free-nodes](gml-hy-n.no-free-nodes.md)  | Draft  | A.1.7 |
| [gml-hy-n.object-references](gml-hy-n.object-references.md)  | Draft  | A.1.8  |
| [gml-hy-n.representation-consistency](gml-hy-n.representation-consistency.md)  | Draft  | A.1.7  |
| [gml-hy-n.simple-features](gml-hy-n.simple-features.md)  | Draft  | A.1.7  |
| [gml-hy-n.trs](gml-hy-n.trs.md)  | Draft  | A.2.5  |
| [gml-hy-n.uom](gml-hy-n.uom.md)  | Draft  | A.2.6  |

Note: A test case seems to be missing for A.3.5 (update frequency!)

## XML namespace prefixes <a name="namespaces"></a>

The following prefixes are used to refer to the corresponding XML namespaces in all test descriptions:

Prefix         | Namespace
-------------- | -------------------------------------------------
base           | http://inspire.ec.europa.eu/schemas/base/3.3
gml            | http://www.opengis.net/gml/3.2
hy             | http://inspire.ec.europa.eu/schemas/hy/4.0
hy-n           | http://inspire.ec.europa.eu/schemas/hy-n/4.0
hy-p           | http://inspire.ec.europa.eu/schemas/hy-p/4.0
net            | http://inspire.ec.europa.eu/schemas/net/4.0
wfs            | http://www.opengis.net/wfs/2.0
xsi            | http://www.w3.org/2001/XMLSchema-instance
xlink          | http://www.w3.org/1999/xlink
xml            | http://www.w3.org/XML/1998/namespace