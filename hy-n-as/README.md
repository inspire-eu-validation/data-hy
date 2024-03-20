# Conformance class: Application schema, Hydrography - Network

Conformance class for the requirements associated with the application schema. 

To be able to test this conformance class, the encoding of the data set must be known, i.e. this is a parameterized conformance class. The XPath expressions used in this test suite assume that the GML encoding is used. If used with the GML encoding this conformance class has an indirect dependency to the conformance class "GML application schemas, Hydrography".

This conformance class is part of the [Abstract Test Suite for the INSPIRE Data Specification on Hydrography](.).

## Standardization target type

INSPIRE spatial data set

## Dependencies

### Direct dependencies

none

### Indirect dependencies

An indirect dependency is another conformance class whose requirements must be met by a related resource.

| Specification | Conformance class | Related resource | Parameters |
| ------------- | ----------------- | ---------------- | ---------- |
| [TG DS-HY](./README#ref_TG_DS_HY) | [GML application schemas, Hydrography](../hy-gml) | INSPIRE spatial data set encoded in GML, Hydrography features | n/a |
 
## Feature types <a name="feature-types"></a>

The instantiable feature types in the application schema are:

* HydroNode
* WatercourseLink
* WatercourseLinkSequence
* WatercourseSeparatedCrossing

*Note*: When "features" or "spatial objects" are mentioned in the test cases, this refers only to instances of feature types of this application schema, not to any types specified in any other application schema.

## External document references

The following abbreviations are used in the test text for referring to external documents:

Abbreviation                     | Document name
-------------------------------- | --------------------------------------------------
TG DS-HY <a name="ref_TG_DS_HY"></a>   | [INSPIRE Data Specification on Hydrography – Technical Guidelines](https://knowledge-base.inspire.ec.europa.eu/publications/inspire-data-specification-hydrography-technical-guidelines_en)
TG DS Template <a name="ref_TG_DS_tmpl"></a>   | [INSPIRE Data Specification Template](https://knowledge-base.inspire.ec.europa.eu/publications/data-specifications-template_en)

## Test Cases

| Identifier                                                        | Status   | Test case in [TG DS-HY](#ref_TG_DS_HY)  |
| ----------------------------------------------------------------- | -------- | ------------ |
| [Code list values](./code-list-values.md)  | Draft  | A.1.3, A.6.1  |
| [Constraints](./constraints.md)  | Draft  | A.1.6  |
| [Geometry](./geometry-consistency.md)  | Draft  | A.1.7  |
| [Identifiers and references](./identifier-and-references.md)  | Draft  | A.1.8 |
| [Link centrelines](./link-centrelines.md)  | Draft  | A.1.10  |
| [Network connectivity](./network-connectivity.md)  | Draft  | A.1.11  |

## XML namespace prefixes <a name="namespaces"></a>

The following prefixes are used to refer to the corresponding XML namespaces in all test descriptions:

Prefix         | Namespace
-------------- | -------------------------------------------------
hy-n           | http://inspire.ec.europa.eu/schemas/hy-n/4.0
hy-p           | http://inspire.ec.europa.eu/schemas/hy-p/5.0
net            | http://inspire.ec.europa.eu/schemas/net/5.0
base           | http://inspire.ec.europa.eu/schemas/base/4.0
gml            | http://www.opengis.net/gml/3.2
wfs            | http://www.opengis.net/wfs/2.0
xsi            | http://www.w3.org/2001/XMLSchema-instance
xlink          | http://www.w3.org/1999/xlink
xml            | http://www.w3.org/XML/1998/namespace

