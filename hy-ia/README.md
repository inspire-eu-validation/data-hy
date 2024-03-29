# Conformance class: Information accessibility, Hydrography

Conformance class for the requirements related to the accessibility of referenced information, for example, information stored in registries (code lists, coordinate reference systems).

To be able to test this conformance class, the encoding of the data set must be known, i.e. this is a parameterized conformance class. The XPath expressions used in this test suite assume that the GML encoding is used. If used with the GML encoding this conformance class has an indirect dependency to the conformance class "GML application schemas, Hydrography".

This conformance class is part of the [Abstract Test Suite for the INSPIRE Data Specification on Hydrography](http://inspire.ec.europa.eu/id/ats/data-hy).

## Standardization target type

INSPIRE spatial data set

## Dependencies

### Direct dependencies

A direct dependency is another conformance class whose requirements must be met by the data set, too.

| Specification | Conformance class | Parameters | 
| ------------- | ----------------- | ---------- |
| [TG DS Template](./README.md#ref_TG_DS_tmpl) | [Information accessibility](http://inspire.ec.europa.eu/id/ats/data/master/information-accessibility) | n/a |

### Indirect dependencies

An indirect dependency is another conformance class whose requirements must be met by a related resource.

| Specification | Conformance class | Related resource | Parameters |
| ------------- | ----------------- | ---------------- | ---------- |
| [TG DS-HY](./README#ref_TG_DS_HY) | [GML application schemas, Hydrography](../hy-gml) | INSPIRE spatial data set encoded in GML, Hydrography features | n/a |
 
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
| [Code lists](./code-list.md)  | ready for review  | A.6.1 |
| [Feature references](./features.md)  | ready for review  | A.1.4 |

## XML namespace prefixes <a name="namespaces"></a>

The following prefixes are used to refer to the corresponding XML namespaces in all test descriptions:

Prefix         | Namespace
-------------- | -------------------------------------------------
gml            | http://www.opengis.net/gml/3.2
hy-n           | http://inspire.ec.europa.eu/schemas/hy-n/4.0
hy-p           | http://inspire.ec.europa.eu/schemas/hy-p/5.0

The following variables are used to refer to the corresponding Xpath expressions in all test descriptions:

Variable       | Value
-------------- | -------------------------------------------------
$features      |  //schema-element(hy-n:HydroNode) \| //schema-element(hy-n:WatercourseLink) \| //schema-element(hy-n:WatercourseLinkSequence) \| //schema-element(hy-n:WatercourseSeparatedCrossing) \| //schema-element(hy-p:Watercourse) \| //schema-element(hy-p:StandingWater) \| //schema-element(hy-p:Wetland) \| //schema-element(hy-p:GlacierSnowfield) \| //schema-element(hy-p:Shore) \| //schema-element(hy-p:DrainageBasin) \| //schema-element(hy-p:RiverBasin) \| //schema-element(hy-p:LandWaterBoundary) \| //schema-element(hy-p:Embankment) \| //schema-element(hy-p:Ford) \| //schema-element(hy-p:Lock) \| //schema-element(hy-p:Sluice) \| //schema-element(hy-p:DamOrWeir) \| //schema-element(hy-p:ShorelineConstruction) \| //schema-element(hy-p:Crossing) \| //schema-element(hy-p:SpringOrSeep) \| //schema-element(hy-p:VanishingPoint) \| //schema-element(hy-p:Rapids) \| //schema-element(hy-p:Falls)
