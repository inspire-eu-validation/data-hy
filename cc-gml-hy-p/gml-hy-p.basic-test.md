# gml-hy-p.basic-test

**Version**: 0.1

**Purpose**: Verify that the spatial data set contains at least one Hydro - Physical Waters feature.

**Prerequisites**

* [Conformance Class "INSPIRE GML encoding of spatial objects"](../cc-gml/README.md)

**Test method**

* Verify that the set of [features](#features) in the spatial data set is not empty. Otherwise report [noFeature](#noFeature)

**Reference(s)**: 

n/a

**Test type**: Automated

**Notes**

There is no requirement that we could reference in the Technical Guidelines. Maybe one should be added in the future revision?

## Messages

Identifier  |  Message text (parameters start with '$')
---------------------------------------------------------- | -------------------------------------------------------------------------
noFeature <a name="noFeature"/>  |  The XML documents representing the spatial data set do not contain a 'Hydro - Physical Waters' feature. Therefore, the spatial data set cannot conform to this conformance class.

## Contextual XPath references

The namespace prefixes used as described in [README.md](README.md#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
features <a name="features"></a>   | //schema-element(hy-p:Crossing) \| //schema-element(hy-p:DrainageBasin) \| //schema-element(hy-p:Embankment) \| //schema-element(hy-p:Falls) \| //schema-element(hy-p:FluvialPoint) \| //schema-element(hy-p:Ford) \| //schema-element(hy-p:LandWaterBoundary) \| //schema-element(hy-p:Lock) \| //schema-element(hy-p:Rapids) \| //schema-element(hy-p:RiverBasin) \| //schema-element(hy-p:Shore) \| //schema-element(hy-p:ShorelineConstruction) \| //schema-element(hy-p:Sluice) \| //schema-element(hy-p:SurfaceWater) \| //schema-element(hy-p:Watercourse) \| //schema-element(hy-p:Wetland) |
