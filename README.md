# Abstract Test Suite for the Data Specification on Hydrography

Abstract Test Suite for the Data Specification on Hydrography – Technical Guidelines (version 3.1) and the associated GML application schemas (version 4.0.0) specifying requirements for the interoperability of spatial data sets of the data theme hydrography.

*Note*: This ATS is under development, none of the tests have an official INSPIRE MIG approval.

## Relationship with the Abstract Test Suite in the document

The Technical Guidelines document contains IR requirements (quoting text from the regulation) and additional TG requirements. This is the basis for an Abstract Test Suite contained in the document as Annex A. The following summarizes the current structure:

1. The implementation-independent requirements are specified in regulation 1089/2010 (including its amendments). 

2. The data specification for each theme includes the general requirements from the regulation ("IR requirements"). These copy the regulation text and are only partly tailored to the specific theme or application schema context. 

3. These IR requirements are then grouped in the ATS of the data specification into several conformance classes. Dependencies between the conformance classes are not identified, so they are all independent of each other. The test cases do not reference the IR requirements in the document directly, but it is safe to assume that these will match. 

4. As the IR requirements are implementation-independent, the test cases for them cannot be tested in an automated way and require manual inspection or questions to the data provider.

5. In addition to the IR requirements, each data specification also includes TG requirements. These are all bundled into a single conformance class per application schema without any dependency to any of the other conformance classes. The test cases do not reference the TG requirements, but sections of the TG document.

6. As these conformance classes are used to declare conformance in the spatial data set metadata, they probably have to be used as they are (including their URIs).

7. Several of the requirements have a different standardisation target (i.e. not the spatial data set). Some of the requirements are on the spatial data set metadata or on the view service operating on the spatial data set.

This is an issue as strictly we can only develop an Executable Test Suite with automated tests for the TG conformance classes. This testing would result in quite incomplete tests, in particular as the majority of the TG test cases are not for the spatial data set, but are for the metadata or the view service, and therefore need to be part of a separate conformance class anyhow. I.e. there would mainly be tests for XML schema validation and CRS URIs.

This would not be a satisfactory result.

In order to proceed towards a more satisfactory solution, the following interpretation is used:

1. Every data specification will only have a single (tested) conformance class per application schema with instantiable spatial object types with the spatial data set as the standardization target. This is basically the TG conformance class, with the changes described below.

2. The TG conformance class is restructured to include tests for all IR requirements and TG requirements that have the spatial data set as the standardization target. The IR requirements are tested under the assumption that the (mandatory) default encoding is used, i.e. in general the GML encoding. Where this is not possible, there will be a manual test.

3. We remove the metadata and view service requirements from the TG conformance class and create new conformance classes for those standardization targets. Again, the requriements would be tested under the assumption that ISO/TS 19139 is used (for the metadata) and that WMS 1.3.0 is used (for the view service).

4. We move all generic GML tests into a new INSPIRE GML conformance class (that should become part of D2.7 in a future revision) and which all other TG conformance classes would normatively reference / depend on.

The TG conformance class is always "informative" in the data specification documents. This is not appropriate, there is no such thing as an informative requirement. For a TG, which the data specifications are, the TG requirements are normative and so should be the TG conformance classes.

## Conformance classes

* [INSPIRE GML encoding of spatial objects](cc-gml/README.md) 
* [GML encoding of application schema 'Hydro - Network', version 4.0](cc-gml-hy-n/README.md)
* [GML encoding of application schema 'Hydro - Physical Waters', version 4.0](cc-gml-hy-p/README.md)

The conformance class 'INSPIRE GML encoding of spatial objects' is only temporary in this Abstract Test Suite and will be moved to its own Abstract Test Suite for the 'Guidelines for the encoding of spatial data' document.

## External document references

The following abbreviations are used in the test text for referring to external documents:

Abbreviation                     | Document name
-------------------------------- | --------------------------------------------------
INSPIRE <a name="ref_INSPIRE"></a> | [Directive 2007/2/EC of the European Parliament and of the Council of 14 March 2007 establishing an Infrastructure for Spatial Information in the European Community (INSPIRE)](http://eur-lex.europa.eu/legal-content/EN/TXT/PDF/?uri=CELEX:32007L0002&from=EN)
D2.7 <a name="ref_D2_7"></a>   | [INSPIRE Guidelines for the encoding of spatial data version 3.3](http://inspire.jrc.ec.europa.eu/documents/Data_Specifications/D2.7_v3.3.pdf)
TG DS-HY <a name="ref_TG_DS_HY"></a>   | [INSPIRE Data Specification on Hydrography – Technical Guidelines version 3.1](http://inspire.ec.europa.eu/documents/Data_Specifications/INSPIRE_DataSpecification_HY_v3.1.pdf)
IR ISDSS <a name="ref_IR_ISDSS"></a>   | [COMMISSION REGULATION (EU) No 1089/2010 of 23 November 2010
implementing Directive 2007/2/EC of the European Parliament and of the Council as regards interoperability of spatial data sets and services](http://eur-lex.europa.eu/legal-content/EN/TXT/PDF/?uri=OJ:L:2010:323:FULL&from=EN)
IR ISDSS Amd 1 <a name="ref_IR_ISDSS_Amd1"></a>   | [COMMISSION REGULATION (EU) No 102/2011 of 4 February 2011
amending Regulation (EU) No 1089/2010 implementing Directive 2007/2/EC of the European Parliament and of the Council as regards interoperability of spatial data sets and services](http://eur-lex.europa.eu/legal-content/EN/TXT/PDF/?uri=CELEX:32011R0102&from=EN)
IR ISDSS Amd 2 <a name="ref_IR_ISDSS_Amd2"></a>   | [COMMISSION REGULATION (EU) No 1253/2013 of 21 October 2013 amending Regulation (EU) No 1089/2010 implementing Directive 2007/2/EC as regards interoperability of spatial data sets and services](http://eur-lex.europa.eu/LexUriServ/LexUriServ.do?uri=OJ:L:2013:331:0001:0267:EN:PDF)