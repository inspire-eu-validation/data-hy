# Basic test

**Version**: 1

**Purpose**: Verify that the spatial data set contains at least one Hydrographic feature.

**Prerequisites**

**Test method**

* Check that the set of [features](#features) in the spatial data set is not empty. Otherwise report [noFeature](#noFeature)

**Reference(s)**: 

* [TG DS-HY](http://inspire.ec.europa.eu/id/ats/data-hy/3.1/hy-gml/README#ref_TG_DS_HY) 5.4, 5.5

**Test type**: Automated

**Notes**

There is no requirement that we could reference in the Technical Guidelines, but such a requirement is clearly missing for any data set with hydrographic features. Maybe such a requirement should be added in the future revision?

## Messages

Identifier  |  Message text (parameters start with '$')
----------- | -------------------------------------------------------------------------
noFeature <a name="noFeature"/>  |  	The XML documents representing the spatial data set do not contain a feature of any of the spatial object types in the 'Hydrography - Physical Waters' or 'Hydrography - Network' application schemas. Therefore, the spatial data set cannot conform to this conformance class. If you have expected to find spatial objects from the application schema in the data set, please consult the statistics information to see the spatial object types that have been found.

## Contextual XPath references

The namespace prefixes used as described in [README.md](http://inspire.ec.europa.eu/id/ats/data-hy/3.1/hy-gml/README#namespaces).

Abbreviation                                          |  XPath expression
----------------------------------------------------- | ------------------------------------------------------------------
features <a name="features"></a>   |  //schema-element(hy-n:HydroNode) \| //schema-element(hy-n:WatercourseLink) \| //schema-element(hy-n:WatercourseLinkSequence) \| //schema-element(hy-n:WatercourseSeparatedCrossing) \| //schema-element(hy-p:Watercourse) \| //schema-element(hy-p:StandingWater) \| //schema-element(hy-p:Wetland) \| //schema-element(hy-p:GlacierSnowfield) \| //schema-element(hy-p:Shore) \| //schema-element(hy-p:DrainageBasin) \| //schema-element(hy-p:RiverBasin) \| //schema-element(hy-p:LandWaterBoundary) \| //schema-element(hy-p:Embankment) \| //schema-element(hy-p:Ford) \| //schema-element(hy-p:Lock) \| //schema-element(hy-p:Sluice) \| //schema-element(hy-p:DamOrWeir) \| //schema-element(hy-p:ShorelineConstruction) \| //schema-element(hy-p:Crossing) \| //schema-element(hy-p:SpringOrSeep) \| //schema-element(hy-p:VanishingPoint) \| //schema-element(hy-p:Rapids) \| //schema-element(hy-p:Falls)