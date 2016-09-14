# Code list values

**Version**: 1

**Purpose**: Verify whether all attributes whose value type is a code list take the values set out therein

**Prerequisites**

**Test method**

When an attribute has a code list as its type, verify that the values comply with the definitions and include the values set out in Annex II of the regulation. To pass this tests that any instance of an attribute

* takes only values explicitly specified in the INSPIRE code list register when the code list‘s extensibility is 'none'.
* takes only a value explicitly specified in the INSPIRE code list register or shall take a value that is narrower (i.e. more specific) than those explicitly specified in the application schema when the code list‘s extensibility is 'narrower'.

Otherwise report [disallowedCodeListValue](#disallowedCodeListValue).

In the Hydrography - Physical Waters application schema, the following properties have to be tested:
* [condition (v3)](#condition3). Valid values:
  * disused 
  * functional
  * projected
  * underConstruction
  * decommissioned
* [condition (v4)](#condition4). Valid values:
  * http://inspire.ec.europa.eu/codelist/ConditionOfFacilityValue/disused 
  * http://inspire.ec.europa.eu/codelist/ConditionOfFacilityValue/functional
  * http://inspire.ec.europa.eu/codelist/ConditionOfFacilityValue/projected
  * http://inspire.ec.europa.eu/codelist/ConditionOfFacilityValue/underConstruction
  * http://inspire.ec.europa.eu/codelist/ConditionOfFacilityValue/decommissioned
* [type (v3)](#type3). Valid values:
  * aqueduct
  * bridge
  * culvert
  * siphon
* [type (v4)](#type4). Valid values:
  * http://inspire.ec.europa.eu/codelist/CrossingTypeValue/aqueduct
  * http://inspire.ec.europa.eu/codelist/CrossingTypeValue/bridge
  * http://inspire.ec.europa.eu/codelist/CrossingTypeValue/culvert
  * http://inspire.ec.europa.eu/codelist/CrossingTypeValue/siphon
* [level (v3)](#level3). Valid values:
  * equinoctialSpringLowWater
  * higherHighWater
  * higherHighWaterLargeTide
  * highestAstronomicalTide
  * highestHighWater
  * highWater
  * highWaterSprings
  * indianSpringHighWater
  * indianSpringLowWater
  * localDatum
  * lowerLowWater
  * lowerLowWaterLargeTide
  * lowestAstronomicalTide
  * lowestLowWater
  * lowestLowWaterSprings
  * lowWater
  * lowWaterDatum
  * lowWaterSprings
  * meanHigherHighWater
  * meanHigherHighWaterSprings
  * meanHigherLowWater
  * meanHighWater
  * meanHighWaterNeaps
  * meanHighWaterSprings
  * meanLowerHighWater
  * meanLowerLowWater
  * meanLowerLowWaterSprings
  * meanLowWater
  * meanLowWaterNeaps
  * meanLowWaterSprings
  * meanSeaLevel
  * meanTideLevel
  * meanWaterLevel
  * nearlyHighestHighWater
  * nearlyLowestLowWater
  * tropicHigherHighWater
  * tropicLowerLowWater
* [level (v4)](#level4). Valid values:
  * http://inspire.ec.europa.eu/codelist/WaterLevelValue/equinoctialSpringLowWater
  * http://inspire.ec.europa.eu/codelist/WaterLevelValue/higherHighWater
  * http://inspire.ec.europa.eu/codelist/WaterLevelValue/higherHighWaterLargeTide
  * http://inspire.ec.europa.eu/codelist/WaterLevelValue/highestAstronomicalTide
  * http://inspire.ec.europa.eu/codelist/WaterLevelValue/highestHighWater
  * http://inspire.ec.europa.eu/codelist/WaterLevelValue/highWater
  * http://inspire.ec.europa.eu/codelist/WaterLevelValue/highWaterSprings
  * http://inspire.ec.europa.eu/codelist/WaterLevelValue/indianSpringHighWater
  * http://inspire.ec.europa.eu/codelist/WaterLevelValue/indianSpringLowWater
  * http://inspire.ec.europa.eu/codelist/WaterLevelValue/localDatum
  * http://inspire.ec.europa.eu/codelist/WaterLevelValue/lowerLowWater
  * http://inspire.ec.europa.eu/codelist/WaterLevelValue/lowerLowWaterLargeTide
  * http://inspire.ec.europa.eu/codelist/WaterLevelValue/lowestAstronomicalTide
  * http://inspire.ec.europa.eu/codelist/WaterLevelValue/lowestLowWater
  * http://inspire.ec.europa.eu/codelist/WaterLevelValue/lowestLowWaterSprings
  * http://inspire.ec.europa.eu/codelist/WaterLevelValue/lowWater
  * http://inspire.ec.europa.eu/codelist/WaterLevelValue/lowWaterDatum
  * http://inspire.ec.europa.eu/codelist/WaterLevelValue/lowWaterSprings
  * http://inspire.ec.europa.eu/codelist/WaterLevelValue/meanHigherHighWater
  * http://inspire.ec.europa.eu/codelist/WaterLevelValue/meanHigherHighWaterSprings
  * http://inspire.ec.europa.eu/codelist/WaterLevelValue/meanHigherLowWater
  * http://inspire.ec.europa.eu/codelist/WaterLevelValue/meanHighWater
  * http://inspire.ec.europa.eu/codelist/WaterLevelValue/meanHighWaterNeaps
  * http://inspire.ec.europa.eu/codelist/WaterLevelValue/meanHighWaterSprings
  * http://inspire.ec.europa.eu/codelist/WaterLevelValue/meanLowerHighWater
  * http://inspire.ec.europa.eu/codelist/WaterLevelValue/meanLowerLowWater
  * http://inspire.ec.europa.eu/codelist/WaterLevelValue/meanLowerLowWaterSprings
  * http://inspire.ec.europa.eu/codelist/WaterLevelValue/meanLowWater
  * http://inspire.ec.europa.eu/codelist/WaterLevelValue/meanLowWaterNeaps
  * http://inspire.ec.europa.eu/codelist/WaterLevelValue/meanLowWaterSprings
  * http://inspire.ec.europa.eu/codelist/WaterLevelValue/meanSeaLevel
  * http://inspire.ec.europa.eu/codelist/WaterLevelValue/meanTideLevel
  * http://inspire.ec.europa.eu/codelist/WaterLevelValue/meanWaterLevel
  * http://inspire.ec.europa.eu/codelist/WaterLevelValue/nearlyHighestHighWater
  * http://inspire.ec.europa.eu/codelist/WaterLevelValue/nearlyLowestLowWater
  * http://inspire.ec.europa.eu/codelist/WaterLevelValue/tropicHigherHighWater
  * http://inspire.ec.europa.eu/codelist/WaterLevelValue/tropicLowerLowWater
* [composition (v3)](#composition3). Valid values:
  * boulders
  * clay
  * gravel
  * mud
  * rock
  * sand
  * shingle 
  * stone
* [composition (v4)](#composition3). Valid values:
  * http://inspire.ec.europa.eu/codelist/ShoreTypeValue/boulders
  * http://inspire.ec.europa.eu/codelist/ShoreTypeValue/clay
  * http://inspire.ec.europa.eu/codelist/ShoreTypeValue/gravel
  * http://inspire.ec.europa.eu/codelist/ShoreTypeValue/mud
  * http://inspire.ec.europa.eu/codelist/ShoreTypeValue/rock
  * http://inspire.ec.europa.eu/codelist/ShoreTypeValue/sand
  * http://inspire.ec.europa.eu/codelist/ShoreTypeValue/shingle 
  * http://inspire.ec.europa.eu/codelist/ShoreTypeValue/stone
* [persistence (v3)](#persistence3). Valid values:
  * dry
  * ephemeral
  * intermittent
  * perennial
* [persistence (v4)](#persistence4). Valid values:
  * http://inspire.ec.europa.eu/codelist/HydrologicalPersistenceValue/dry
  * http://inspire.ec.europa.eu/codelist/HydrologicalPersistenceValue/ephemeral
  * http://inspire.ec.europa.eu/codelist/HydrologicalPersistenceValue/intermittent
  * http://inspire.ec.europa.eu/codelist/HydrologicalPersistenceValue/perennial

The following is not applicable for this application schema as no extensions are allowed. It is still included here as a reminder in case extensions will be allowed in the future:

Inspect the code list valued property elements. If a value is not one of the values listed above, review the code list definition to check that any extensions do not overlap with the code lists that are defined in Annexes II, III and IV of the Implementing Rule and that all extensions conform to the requirements. This is a manual test.
  
**Reference(s)**: 

* [TG DS Template](http://inspire.ec.europa.eu/id/ats/data-hy/3.1/hy-p-as/README#ref_TG_DS_tmpl) IR requirement Article 4 (1)
* [TG DS Template](http://inspire.ec.europa.eu/id/ats/data-hy/3.1/hy-p-as/README#ref_TG_DS_tmpl) IR requirement Article 4 (3)
* [TG DS Template](http://inspire.ec.europa.eu/id/ats/data-hy/3.1/hy-p-as/README#ref_TG_DS_tmpl) IR requirement Article 6 (1)
* [TG DS Template](http://inspire.ec.europa.eu/id/ats/data-hy/3.1/hy-p-as/README#ref_TG_DS_tmpl) IR requirement Article 6 (2)
* [TG DS Template](http://inspire.ec.europa.eu/id/ats/data-hy/3.1/hy-p-as/README#ref_TG_DS_tmpl) IR requirement Article 6 (3)
* [TG DS Template](http://inspire.ec.europa.eu/id/ats/data-hy/3.1/hy-p-as/README#ref_TG_DS_tmpl) IR requirement Article 6 (4)

**Test type**: Automated

**Notes**

## Messages

Identifier  |  Message text (parameters start with '$')
---------------------------------------------------------- | -------------------------------------------------------------------------
disallowedCodeListValue <a name="disallowedCodeListValue"/>  |  XML document '$filename', $featureType '$gmlid': The property '$propertyName' has a value '$value' that is not one of the allowed values listed at $codelist. 

## Contextual XPath references

The namespace prefixes used as described in [README.md](http://inspire.ec.europa.eu/id/ats/data-hy/3.1/hy-p-as/README#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
condition (v3) <a name="condition3"></a> |  //schema-element(hy-p3:Crossing)/hy-p3:condition/text() \| //schema-element(hy-p3:DamOrWeir)/hy-p3:condition/text() \| //schema-element(hy-p3:Embankment)/hy-p3:condition/text() \| //schema-element(hy-p3:Ford)/hy-p3:condition/text() \| //schema-element(hy-p3:Lock)/hy-p3:condition/text() \| //schema-element(hy-p3:ShorelineConstruction)/hy-p3:condition/text() \| //schema-element(hy-p3:Sluice)/hy-p3:condition/text() \| //schema-element(hy-p3:Watercourse)/hy-p3:condition/text()
condition (v4) <a name="condition4"></a> |  //schema-element(hy-p4:Crossing)/hy-p4:condition/@xlink:href \| //schema-element(hy-p4:DamOrWeir)/hy-p4:condition/@xlink:href \| //schema-element(hy-p4:Embankment)/hy-p4:condition/@xlink:href \| //schema-element(hy-p4:Ford)/hy-p4:condition/@xlink:href \| //schema-element(hy-p4:Lock)/hy-p4:condition/@xlink:href \| //schema-element(hy-p4:ShorelineConstruction)/hy-p4:condition/@xlink:href \| //schema-element(hy-p4:Sluice)/hy-p4:condition/@xlink:href \| //schema-element(hy-p4:Watercourse)/hy-p4:condition/@xlink:href
type (v3) <a name="type3"></a> |  //schema-element(hy-p3:Crossing)/hy-p3:type/text()
type (v4) <a name="type4"></a> |  //schema-element(hy-p4:Crossing)/hy-p4:type/@xlink:href
level (v3) <a name="level3"></a> |  //schema-element(hy-p3:LandWaterBoundary)/hy-p3:waterLevelCategory/text()
level (v4) <a name="level4"></a> |  //schema-element(hy-p4:LandWaterBoundary)/hy-p4:waterLevelCategory/@xlink:href
composition (v3) <a name="composition3"></a> |  //schema-element(hy-p3:Shore)/hy-p3:composition/text()
composition (v4) <a name="composition4"></a> |  //schema-element(hy-p4:Shore)/hy-p4:composition/@xlink:href
persistence (v3) <a name="persistence3"></a> |  //schema-element(hy-p3:StandingWater)/hy-p3:persistence/text() \| //schema-element(hy-p3:Watercourse)/hy-p3:persistence/text()
persistence (v4) <a name="persistence4"></a> |  //schema-element(hy-p4:StandingWater)/hy-p4:persistence/@xlink:href \| //schema-element(hy-p4:Watercourse)/hy-p4:persistence/@xlink:href

