# Abstract Test Suite for the Data Specification on Hydrography

Abstract Test Suite for the Data Specification on Hydrography – Technical Guidelines (version 3.1) and the associated GML application schemas (versions 3.0 and 4.0) specifying requirements for the interoperability of spatial data sets of the data theme hydrography.

*Note*: This ATS is under development, none of the tests have an official INSPIRE MIG approval.

## Approach

We have used the following approach:

1. There is one GML conformance class per application schema with non-abstract spatial object types. This is basically the "encoding schema validation test" from the TG conformance class in the data specifications. 

2. In order to make the IR conformance classes testable, they are understood as parameterized conformance classes with the encoding rule as the parameter. Note: The concept of parameterized conformance classes is described in the [OGC Specification Model](https://portal.opengeospatial.org/files/?artifact_id=34762).

3. All XPath expressions in the IR conformance classes are based on the default GML encoding rule. I.e., the current versions of the IR conformance classes are parametrized with the default GML encoding rule and have an indirect dependency to the GML application schema conformance class.  

4. As a result, there is no need for an encoding-related IR conformance class. Instead, the details how to test the conformance for any additional encoding rule would need to be added to the relevant tests and a new conformance class for the validation against the schemas would be added.

5. The IR conformance classes for application schemas without non-abstract feature types, e.g. "Hydrography - Core", are not needed as no feature instance can be of a type from that application schema.

6. All generic tests related to the GML encoding rule are moved to a new INSPIRE GML conformance class (that should become part of D2.7 in a future revision) and which all other TG conformance classes would normatively reference / depend on.

7. The conformance classes with a different standardization target are not included for now. Only the requirements on a data set resource are included.

Note that the TG conformance class is "informative" in the data specification documents. This is not appropriate, there is no such thing as an informative requirement. For a TG, which the data specifications are, the TG requirements are normative and so should be the TG conformance classes.

## Conformance classes

The following conformance classes related to the spatial data set have been identified as a result:

* [Conformance class "INSPIRE GML encoding rule 3.3"](inspire-gml/README.md) 
* [Conformance class "GML application schema, Hydrography - Network 3.0/4.0"](gml-hy-n/README.md)
* [Conformance class "Application schema, Hydrography - Network 3.1"](hy-n-as/README.md)
* [Conformance class "Reference Systems, Hydrography - Network 3.1"](hy-n-rs/README.md)
* [Conformance class "Data Consistency, Hydrography - Network 3.1"](hy-n-dc/README.md)
* [Conformance class "Information Accessibility, Hydrography - Network 3.1"](hy-n-ia/README.md)
* Conformance class "GML application schema, Hydrography - Physical Waters 3.0/4.0"
* Conformance class "Application schema, Hydrography - Physical Waters 3.1"
* Conformance class "Reference Systems, Hydrography - Physical Waters 3.1"
* Conformance class "Data Consistency, Hydrography - Physical Waters 3.1"
* Conformance class "Information Accessibility, Hydrography - Physical Waters 3.1"

The conformance class 'INSPIRE GML encoding rule 3.3' is only temporary in this Abstract Test Suite and belongs to its own Abstract Test Suite for the 'Guidelines for the encoding of spatial data' document.

The conformance classes related to the 'Physical Waters' schema have not been created yet, but they would follow the same pattern as the network schema tests.

The conformance class regarding the metadata for interoperability is currently documented in a [separate ATS](https://github.com/inspire-eu-validation/ats-interoperability-metadata). Note that the MIWP-5 work has created a single conformance class, independent of the application schema, while each data specification currently specifies a separate conformance class. 

The conformance class regarding the view service portrayal still has to be created.

## Example

To illustrate and test the approach, draft XQuery-based executable test suites have been created for the conformance classes documented in this ATS. The test suites have been created using ETF as the framework and BaseX as the test engine. This has some limitations with respect to the support for the domain model specified in the current design report (version 0.3) as ETF does not yet support all aspects. For example, 'manual tests' have been classified as a 'warning' as ETF currently does not support this concept. The test project with the definitions of the executable test suites is **[hy-n-assertions.xml](hy-n-assertions.xml)**.

A **[small test data set](data/README.md)** has been accessed from an INSPIRE download service. 

Using the executable test suites and the sample test data set, a **[test report](wfs-es-hy-n-result.html)** for the test of this sample data set against the conformance classes has been created.
