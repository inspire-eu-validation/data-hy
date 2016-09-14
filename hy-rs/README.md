# Conformance class: Reference systems, Hydrography (DRAFT)

Conformance class for the requirements associated with reference systems (spatial and temporal, units of measurement).

To be able to test this conformance class, the encoding of the data set must be known, i.e. this is a parameterized conformance class. The XPath expressions used in this test suite assume that the GML encoding is used. If used with the GML encoding this conformance class has an indirect dependency to the conformance class "GML application schemas, Hydrography".

This conformance class is part of the [Abstract Test Suite for the INSPIRE Data Specification on Hydrography](http://inspire.ec.europa.eu/id/ats/data-hy/3.1).

## Standardization target type

INSPIRE spatial data set

## Dependencies

### Direct dependencies

A direct dependency is another conformance class whose requirements must be met by the data set, too.

| Specification | Conformance class | Parameters | 
| ------------- | ----------------- | ---------- |
| [TG DS Template](http://inspire.ec.europa.eu/id/ats/data-hy/3.1/hy-ia/README#ref_TG_DS_tmpl) | [Information accessibility](http://inspire.ec.europa.eu/id/ats/data/3.0rc3/information-accessibility) | n/a |

### Indirect dependencies

An indirect dependency is another conformance class whose requirements must be met by a related resource.

| Specification | Conformance class | Related resource | Parameters |
| ------------- | ----------------- | ---------------- | ---------- |
| [TG DS-HY](http://inspire.ec.europa.eu/id/ats/data-hy/3.1/hy-rs/README#ref_TG_DS_HY) | [GML application schemas, Hydrography](http://inspire.ec.europa.eu/id/ats/data-hy/3.1/hy-gml) | INSPIRE spatial data set encoded in GML, Hydrography features | n/a |
 
## Feature types <a name="feature-types"></a>

TThe instantiable feature types are:
 
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
TG DS-HY <a name="ref_TG_DS_HY"></a>   | [INSPIRE Data Specification on Hydrography – Technical Guidelines version 3.1](http://inspire.ec.europa.eu/documents/Data_Specifications/INSPIRE_DataSpecification_HY_v3.1.pdf)
TG DS Template <a name="ref_TG_DS_tmpl"></a>   | [INSPIRE Data Specification Template version 3.0rc3](http://inspire.jrc.ec.europa.eu/documents/Data_Specifications/INSPIRE_DataSpecification_Template_v3.0rc3.pdf)

## Test Cases

| Identifier                                                        | Status   | Test case in [TG DS-HY](#ref_TG_DS_HY)  |
| ----------------------------------------------------------------- | -------- | ------------ |
| [Units of measure](http://inspire.ec.europa.eu/id/ats/data-hy/3.1/hy-rs/uom)  | ready for review  | A.2.6  |

## XML namespace prefixes <a name="namespaces"></a>

The following prefixes are used to refer to the corresponding XML namespaces in all test descriptions:

Prefix         | Namespace
-------------- | -------------------------------------------------
gml            | http://www.opengis.net/gml/3.2
hy-n           | urn:x-inspire:specification:gmlas:HydroNetwork:3.0 or http://inspire.ec.europa.eu/schemas/hy-n/4.0
hy-p           | urn:x-inspire:specification:gmlas:HydroPhysicalWaters:3.0 or http://inspire.ec.europa.eu/schemas/hy-p/4.0

The following variables are used to refer to the corresponding Xpath expressions in all test descriptions:

Variable       | Value
-------------- | -------------------------------------------------
$features      |  //schema-element(hy-n:HydroNode) \| //schema-element(hy-n:WatercourseLink) \| //schema-element(hy-n:WatercourseLinkSequence) \| //schema-element(hy-n:WatercourseSeparatedCrossing) \| //schema-element(hy-p:Watercourse) \| //schema-element(hy-p:StandingWater) \| //schema-element(hy-p:Wetland) \| //schema-element(hy-p:GlacierSnowfield) \| //schema-element(hy-p:Shore) \| //schema-element(hy-p:DrainageBasin) \| //schema-element(hy-p:RiverBasin) \| //schema-element(hy-p:LandWaterBoundary) \| //schema-element(hy-p:Embankment) \| //schema-element(hy-p:Ford) \| //schema-element(hy-p:Lock) \| //schema-element(hy-p:Sluice) \| //schema-element(hy-p:DamOrWeir) \| //schema-element(hy-p:ShorelineConstruction) \| //schema-element(hy-p:Crossing) \| //schema-element(hy-p:SpringOrSeep) \| //schema-element(hy-p:VanishingPoint) \| //schema-element(hy-p:Rapids) \| //schema-element(hy-p:Falls)
