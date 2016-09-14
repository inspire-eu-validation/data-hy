# Conformance class: Application schema, Hydrography - Physical Waters (DRAFT)

Conformance class for the requirements associated with the application schema. 

To be able to test this conformance class, the encoding of the data set must be known, i.e. this is a parameterized conformance class. The XPath expressions used in this test suite assume that the GML encoding is used. If used with the GML encoding this conformance class has an indirect dependency to the conformance class "GML application schemas, Hydrography".

This conformance class is part of the [Abstract Test Suite for the INSPIRE Data Specification on Hydrography](http://inspire.ec.europa.eu/id/ats/data-hy/3.1).

## Standardization target type

INSPIRE spatial data set

## Dependencies

### Direct dependencies

none

### Indirect dependencies

An indirect dependency is another conformance class whose requirements must be met by a related resource.

| Specification | Conformance class | Related resource | Parameters |
| ------------- | ----------------- | ---------------- | ---------- |
| [TG DS-HY](http://inspire.ec.europa.eu/id/ats/data-hy/3.1/hy-p-as/README#ref_TG_DS_HY) | [GML application schemas, Hydrography](http://inspire.ec.europa.eu/id/ats/data-hy/3.1/hy-gml) | INSPIRE spatial data set encoded in GML, Hydrography features | n/a |
 
## Feature types <a name="feature-types"></a>

The instantiable feature types in the application schema are:

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
| [Code list values](http://inspire.ec.europa.eu/id/ats/data-hy/3.1/hy-p-as/code-list-values)  | Draft  | A.1.3, A.6.1  |
| [Constraints](http://inspire.ec.europa.eu/id/ats/data-hy/3.1/hy-p-as/constraints)  | Draft  | A.1.6  |
| [Geometry](http://inspire.ec.europa.eu/id/ats/data-hy/3.1/hy-p-as/geometry)  | Draft  | A.1.7  |
| [Identifiers and references](http://inspire.ec.europa.eu/id/ats/data-hy/3.1/hy-p-as/identifier-and-references)  | Draft  | A.1.8 |

## XML namespace prefixes <a name="namespaces"></a>

The following prefixes are used to refer to the corresponding XML namespaces in all test descriptions:

Prefix         | Namespace
-------------- | -------------------------------------------------
hy-p3          | urn:x-inspire:specification:gmlas:HydroPhysicalWaters:3.0
hy-p4          | http://inspire.ec.europa.eu/schemas/hy-p/4.0
base           | http://inspire.ec.europa.eu/schemas/base/3.3
gml            | http://www.opengis.net/gml/3.2
net3           | urn:x-inspire:specification:gmlas:Network:3.2
net4           | http://inspire.ec.europa.eu/schemas/net/4.0
wfs            | http://www.opengis.net/wfs/2.0
xsi            | http://www.w3.org/2001/XMLSchema-instance
xlink          | http://www.w3.org/1999/xlink
xml            | http://www.w3.org/XML/1998/namespace