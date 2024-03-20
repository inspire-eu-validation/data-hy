# Conformance class: Data consistency, Hydrography

Conformance class for the requirements related to the consistency of the data.

To be able to test this conformance class, the encoding of the data set must be known, i.e. this is a parameterized conformance class. The XPath expressions used in this test suite assume that the GML encoding is used. If used with the GML encoding this conformance class has an indirect dependency to the conformance class "GML application schemas, Hydrography".

This conformance class is part of the [Abstract Test Suite for the INSPIRE Data Specification on Hydrography](http://inspire.ec.europa.eu/id/ats/data-hy).

## Standardization target type

INSPIRE spatial data set

## Dependencies

### Direct dependencies

A direct dependency is another conformance class whose requirements must be met by the data set, too.

| Specification | Conformance class | Parameters | 
| ------------- | ----------------- | ---------- |
| [TG DS Template](./README#ref_TG_DS_tmpl) | [Data consistency](http://inspire.ec.europa.eu/id/ats/data/master/data-consistency) | n/a |

### Indirect dependencies

An indirect dependency is another conformance class whose requirements must be met by a related resource.

| Specification | Conformance class | Related resource | Parameters |
| ------------- | ----------------- | ---------------- | ---------- |
| [TG DS-HY](../hy-n-as/README.md#ref_TG_DS_HY) | [GML application schemas, Hydrography](../hy-gml) | INSPIRE spatial data set encoded in GML, Hydrography features | n/a |
 
## Feature types <a name="feature-types"></a>

The instantiable feature types are:

Network:

* HydroNode
* WatercourseLink
* WatercourseLinkSequence
* WatercourseSeparatedCrossing

Physical Waters:

* Watercourse
* StandingWater
* Wetland
* GlacierSnowfield
* Shore
* DrainageBasin
* RiverBasin
* LandWaterBoundary
* Embankment
* Ford
* Lock
* Sluice
* DamOrWeir
* ShorelineConstruction
* Crossing
* SpringOrSeep
* VanishingPoint
* Rapids
* Falls

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
| [Spatial consistency](./spatial.md)  | ready for review  | A.1.7, A.3.6  |
| [Thematic consistency](./thematic.md)  | ready for review  | A.3.6  |
| [Identifiers](./identifiers.md)  | ready for review  | A.3.7  |

Note: A test case seems to be missing for A.3.5 (update frequency).

## XML namespace prefixes <a name="namespaces"></a>

The following prefixes are used to refer to the corresponding XML namespaces in all test descriptions:

Prefix         | Namespace
-------------- | -------------------------------------------------
hy-n           | http://inspire.ec.europa.eu/schemas/hy-n/4.0
hy-p           | http://inspire.ec.europa.eu/schemas/hy-p/5.0
gml            | http://www.opengis.net/gml/3.2
